# Adaptive design (medicine)

In an adaptive clinical trial, researchers change the trial's parameters mid‑course based on planned interim analyses of accumulating data, rather than locking every decision in place before the first patient is enrolled. The adaptation rules are written into the protocol before the trial starts, so the changes are pre‑specified, not ad hoc. Adaptable elements include the dose, the sample size, the patient selection criteria, the treatment being tested, the randomisation ratio, and the trial's primary endpoint.

The purpose is to identify effective drugs or vaccines faster and to focus on patient populations that actually benefit. Adaptive trials reduce the number of participants exposed to inferior treatments by dropping failing arms early and shifting more patients toward whichever group looks most promising.

## How the design differs from a traditional trial

A traditional randomised trial follows a fixed three‑step pipeline: design the study, run it exactly as written, then analyse the data once enrolment ends. Nothing in the protocol changes after the trial begins. An adaptive trial inserts planned interim analyses at which accumulated data can trigger a pre‑written modification. Everything that may change, and the trigger for changing it, is declared in advance, and the protocol is published so readers can confirm the adaptations were foreseen.

## Common types of adaptive design

| Type | What changes | Core idea |
|------|-------------|-----------|
| Dose‑finding | Treatment dose | Search for the lowest toxic, highest effective dose. Model‑based methods such as the continual reassessment method (CRM) outperform the classic "3+3" rule. |
| Group sequential | Sample size at fixed intervals | Stop for benefit (strong evidence the drug works) or for futility (evidence it does not), or continue. The Simon two‑stage design is the standard single‑arm version; Mander–Thompson allows stopping for either. |
| Response adaptive randomisation | Randomisation ratios | As interim data accumulate, more patients are routed toward the better‑performing arm. |
| Adaptive treatment‑switching | Individual treatment | Patients move between arms by pre‑set rules. |
| Biomarker adaptive / population enrichment | Who is enrolled | Focus on biomarker‑positive sub‑groups once a signal appears. |
| Multi‑arm multi‑stage | Open treatment arms | Underperforming arms stop recruiting; new arms can be added. |
| Platform trial | Treatment arms vs. one shared control | A standing control group is compared against a rotating cast of experimental arms, often indefinitely. |
| Sample size re‑estimation | Total or per‑group size | Adjust size once true effect size is better estimated. |
| Seamless Phase I/II or II/III | Phase boundaries | Safety, dosing, and efficacy are studied in one continuous protocol rather than separate trials. |

Two related efficiency tools shorten trials further. **Non‑stochastic curtailment** stops a trial the moment the final answer is already knowable from the data in hand. **Stochastic curtailment** stops when the probability of eventually reaching that answer crosses a threshold, saving more patients on average.

## Statistical machinery

Because the data are looked at repeatedly, simple p‑values break down. Designs typically use **Bayesian** statistics, which update the probability that a treatment works each time new data arrive. The structure mirrors the **multi‑armed bandit problem** studied in reinforcement learning. For regulatory acceptance, sponsors usually must show that the Bayesian plan also controls the frequentist type I and type II error rates, and they report a **posterior probability** (how likely the drug works given the data so far) and a **predictive probability** (how likely the trial is to succeed if it continues to its maximum size).

## Where adaptive designs have been used

In breast cancer, the I‑SPY series used a shared standard arm and biomarker‑guided randomisation to test many experimental neoadjuvant regimens in parallel. I‑SPY 1 (2002–2006, 237 patients) showed that early tumour shrinkage on MRI predicts long‑term survival, a finding I‑SPY 2 then exploited. I‑SPY 2 links about 20 cancer centres, the FDA, the NCI, and multiple pharmaceutical companies around a single platform, escalating or dropping drugs in real time; graduating regimens can be routed toward FDA Accelerated Approval.

During the 2020 COVID‑19 pandemic, the WHO Solidarity and European Discovery trials applied adaptive methods to test several antivirals simultaneously in hospitalised patients, dropping arms that failed while the trials were still running. The US NIAID launched ACTT, an adaptive international Phase III trial enrolling up to 800 hospitalised patients at around 100 sites. The European EPAD programme, funded at €53 million through the Innovative Medicines Initiative, plans to feed data from a 2,000‑person longitudinal cohort into adaptive prevention trials of about 1,500 participants each, targeting early Alzheimer's.

## Regulatory timeline

The modern era began in 2004, when the US FDA's Strategic Path Initiative called for more flexible trial designs. The FDA issued draft guidance on adaptive design in 2010 and a final version, *Adaptive Design Clinical Trials for Drugs and Biologics*, in 2019. The FDA Center for Veterinary Medicine published parallel guidance for animal drugs in October 2021. The 2012 PCAST report urged the FDA to run pilots of adaptive approval mechanisms that span pre‑ and post‑market phases.

## Costs and limits

Adaptation adds operational and statistical complexity: drug supply, randomisation systems, data capture, and the monitoring of multiple testing all become harder, and any repeated testing inflates type I error unless explicitly controlled. A pre‑specified, publicly registered protocol is the main safeguard against post‑hoc cherry‑picking. Shorter follow‑up can miss long‑term harms, such as cancer recurrence. Adaptive designs are not always worth it: when the primary outcome takes a long time to observe, interim looks at patients who have not yet had an event contribute little, eroding the efficiency gain and increasing the chance that the trial is stopped for futility before a real benefit can be detected.

Source: adapted from "Adaptive design (medicine)" on English Wikipedia, whose text is written by Wikipedia contributors, under CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/): https://en.wikipedia.org/wiki/Adaptive_design_%28medicine%29
