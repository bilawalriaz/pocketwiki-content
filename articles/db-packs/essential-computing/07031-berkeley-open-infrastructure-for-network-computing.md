# Berkeley Open Infrastructure for Network Computing

BOINC (rhymes with "oink") is an open-source middleware system for volunteer computing, a form of distributed computing in which a research project borrows the unused CPU and GPU cycles of ordinary computers owned by the public. Its job is to make that donation portable across operating systems, reusable across many unrelated projects from the same client, and resistant to cheating.

## How it works

A research group writes a scientific application, splits its calculations into small work units, and runs a BOINC server. Volunteers install the BOINC client on a PC, phone, or tablet, pick which projects to support, and let the client download work units, compute them when the device is idle, and return results. The server validates the answers, awards credit, and sends more work.

The system has two halves: a server that holds the work queue and validates returned results, and a client that fetches work, runs it, and reports back. BOINC is written in C++ for the client and server, PHP for each project's web management, and Java or Kotlin for the Android client. It runs on Windows, macOS, Linux, Android, FreeBSD, and Raspberry Pi OS, and is released under the GNU Lesser General Public License version 3 or later.

## Origin

BOINC was created at the Space Sciences Laboratory of the University of California, Berkeley, led by David P. Anderson, who also led SETI@home, the radio-telescope search for extraterrestrial intelligence. The original SETI client was a single-project program with weak security; some participants cheated the credit system or submitted fake results. BOINC was designed to fix that, then generalised into a platform any research group could use.

The BOINC project began in February 2002, with the first version released on 10 April 2002. Predictor@home, launched on 9 June 2004, was the first BOINC-based project. In 2009 AQUA@home ran the first multi-threaded CPU application, and in 2010 the first OpenCL application appeared. GPU support arrived through Nvidia's CUDA in 2008 and through OpenCL, with AMD/ATI GPUs added in October 2009; GPU versions typically run 2–10 times faster than the CPU-only versions they replaced. Intel GPU work remains sparse.

## Control, accounts, and credit

A BOINC client can be controlled by remote procedure calls, a command-line tool, or the BOINC Manager, which has a Simplified GUI and an Advanced View (an older Grid View was removed in version 6.6.x).

BOINC Account Managers handle sign-up and project selection across many machines for users who want a simpler experience. Examples include GridRepublic, BAM!, Science United, Charity Engine, and Dazzler.

The BOINC Credit System awards credit only after a result has been validated, typically by being independently re-computed by another volunteer and matched. This double-checking is what keeps bad hardware and cheating from inflating the leaderboards.

## Mobile and external incentive layers

A BOINC app for Android lets phones, tablets, and Kindles contribute. By default it runs only when the device is on Wi-Fi, is charging, and the battery is at least 90% full. Google Play does not host it because each BOINC project ships its own executable, so the app is distributed through the BOINC website and F-Droid.

Independent third parties have built incentive layers on top of BOINC, including Charity Engine (prize draws funded by buyers of donated compute), the now-defunct Bitcoin Utopia, and Gridcoin, a blockchain that mints coins in proportion to BOINC credit earned.

## Projects and scale

BOINC hosts projects across medicine, molecular biology, mathematics, linguistics, climatology, environmental science, and astrophysics. Representative active projects include Einstein@Home (pulsar search using radio and gravitational-wave data), Rosetta@home (protein structure prediction for disease research), LHC@home (simulations for CERN's Large Hadron Collider), climateprediction.net (climate models at Oxford University), MilkyWay@home (galaxy simulation from Sloan Digital Sky Survey data), PrimeGrid (searches for large primes), and World Community Grid, a multi-project effort now at the Krembil Research Institute.

As of 13 August 2026, BOINC combined 25,314 active participants and 130,853 active hosts, delivering on average 15.220 petaFLOPS per day, a figure that would rank 139th on the TOP500 list of supercomputers. Guinness World Records recognises BOINC as the largest computing grid. The platform has been funded in part by the U.S. National Science Foundation, and a voluntary international BOINC Workshop is held each year to coordinate project administrators.

## Trade-offs

Volunteer machines are unpredictable, often offline, and heterogeneous, so projects must write applications that can be checkpointed, resumed, and verified. Mobile projects are restricted to the subset that fits Android, and only projects listed on the official BOINC site contribute to the combined statistics; independent BOINC-based efforts exist outside that list.

Source: adapted from "Berkeley Open Infrastructure for Network Computing" on English Wikipedia, whose text is written by Wikipedia contributors, under CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/): https://en.wikipedia.org/wiki/Berkeley_Open_Infrastructure_for_Network_Computing
