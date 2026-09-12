# Apprenticeship learning

Apprenticeship learning, also called learning from demonstration or imitation learning, is a branch of machine learning in which a system acquires behaviour by watching an expert rather than by being told what to do. It is a form of supervised learning: the training set consists of recorded task executions by a demonstration teacher, and the learner tries to reproduce the demonstrated skill.

# What the learner has to infer

A reinforcement learning agent learns behaviour by maximising a numerical reward signal. In apprenticeship learning the agent is not given that signal. Instead it watches a person perform a task and reverse-engineers the reward function the person appears to be optimising, then plans with that recovered function as if it had been supplied up front. The formal task is: given an agent's behaviour over time, the sensory inputs it received, and a model of its body and environment, determine the reward function it is optimising.

Stuart J. Russell has proposed using this idea to observe humans and codify their ethical values, so that robots could know, for example, not to cook a cat without being explicitly told. The interaction can be modelled as a cooperative inverse reinforcement learning game, in which a human and a robot cooperate to satisfy the human's implicit goals even though neither can state them. In 2017, OpenAI and DeepMind applied deep learning to this cooperative setting in simple domains such as Atari games and basic robot tasks such as backflips, with the human limited to answering which of two candidate actions it preferred, and reported evidence that the approach scales economically to modern systems.

# The three main approaches

Apprenticeship methods can be grouped by what they try to copy directly.

- Mapping approach. The system forms a direct map, either from states to actions or from states to reward values. In 2002, researchers used this approach to teach an AIBO robot basic soccer skills.
- Inverse reinforcement learning (IRL). The system derives a reward function from observed behaviour and then plans with it. A 2004 method called Apprenticeship via Inverse Reinforcement Learning (AIRP), developed by Pieter Abbeel at Berkeley and Andrew Ng at Stanford, handles Markov decision processes (sequential decision problems in which the next state depends only on the current state and action) where the reward function is not given but an expert demonstration is. AIRP fits dynamic tasks such as driving, where safe following distance, steady speed, and infrequent lane changes act at once and a hand-written reward rarely converges to the right policy. Abbeel, Coates, and Ng later used AIRP to model aerobatic helicopter trajectories, including in-place flips, in-place rolls, loops, hurricanes, and auto-rotation landings.
- System model approach. The system models the dynamics of the world rather than the policy itself, and learns rules that associate preconditions and postconditions with each action. A 1994 demonstration had a humanoid learn a generalised plan for a repetitive ball-collection task from only two demonstrations.

# How the demonstration is actually recorded

In a typical setup a robot control system is available and the human demonstrator uses it. The operator moves a robot arm through a task, such as positioning a cup under a coffeemaker and pressing start, and the robot later replays the motion. From the outside, the replay can look like a one-to-one copy of the demonstration, but the internal process is more involved.

A 1997 experiment by Stefan Schaal on the Sarcos robot arm illustrates the mechanism. The goal was to swing up and balance an inverted pendulum, an optimal control problem that is hard to solve with a brute-force search. Schaal instead recorded a human demonstration: the pendulum's angle was logged over three seconds, producing a trajectory of the form:

time (s) | angle (rad)
0.0 | -3.0
0.5 | -2.8
1.0 | -4.5
1.5 | -1.0

Time runs along the horizontal axis and a variable such as position or angle along the vertical, a principle known in computer animation as spline animation. Reproducing the motion is then a tracking or PID control problem: a PID (proportional-integral-derivative) controller reads the current error between the recorded and actual angle and outputs a corrective action, so that control actions chosen step by step drive the system along the recorded trajectory. Other authors describe the same idea as steering behaviour, because the robot is being guided onto a given line. One of the first works on robot apprentices was Adrian Stoica's 1995 PhD thesis on anthropomorphic robots learning by imitation.
