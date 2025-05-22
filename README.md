# Cyber_Terminal-_Speed_Hack
# Cyber Terminal // Speed Hack - README

Welcome, Operator Crash_Override, to the Cyber Terminal Simulation!

This document provides an overview of the game, its features, core gameplay, the extended "Act II" missions, and a guide to the various commands and hidden easter eggs you might encounter.

## Table of Contents

1.  [Game Overview](#game-overview)
2.  [Core Gameplay Loop (Phase I & Phase II)](#core-gameplay-loop-phase-i--phase-ii)
    *   [Phase I: Initial Targets](#phase-i-initial-targets)
    *   [Phase II: The Deep Dive (Extended Targets)](#phase-ii-the-deep-dive-extended-targets)
3.  [Implemented Features & Enhancements](#implemented-features--enhancements)
4.  [Main Commands (Gameplay Progression)](#main-commands-gameplay-progression)
5.  [Utility & Fun Commands (Easter Eggs & More)](#utility--fun-commands-easter-eggs--more)
    *   [Information & System](#information--system)
    *   [File System Interaction (Local & Target)](#file-system-interaction-local--target)
    *   [Network & Fun](#network--fun)
    *   [Developer Parody Tools](#developer-parody-tools)
    *   [System Administration Parody](#system-administration-parody)
6.  [Easter Egg Quick Guide](#easter-egg-quick-guide)
7.  [Future Ideas (Sound Placeholders)](#future-ideas-sound-placeholders)

---

## 1. Game Overview

**Cyber Terminal // Hacking Simulation v2.1** is an immersive text-based hacking game where you take on the role of Operator Crash_Override. Your initial mission, codenamed **Operation 'Global Cascade'**, is to retrieve critical data from multiple high-security targets to uncover a global conspiracy.

But the rabbit hole goes deeper. Should you prove your mettle by evading the initial pursuit, a new set of 10 even more challenging and high-value targets will unlock, pushing your skills to the absolute limit. This is **Phase II: The Deep Dive**.

Navigate file systems, exploit vulnerabilities, download sensitive information, and evade the ever-watchful eyes of system administrators and automated security protocols across multiple stages of escalating intensity. The simulation offers different difficulty levels, affecting timers and the ferocity of the pursuits.

Beyond the main objectives, the terminal is filled with hidden commands, lore snippets, and humorous easter eggs for curious hackers to discover.

---

## 2. Core Gameplay Loop (Phase I & Phase II)

### Phase I: Initial Targets

1.  **Initialization & Briefing:** The game starts with an intro sequence, setting the scene for Operation 'Global Cascade'.
2.  **Difficulty Selection:** Choose your skill level:
    *   **Noob:** A relaxed experience with no timers.
    *   **Expert:** A challenging mode with a 5-minute timer per target.
    *   **Hacker:** The ultimate test with a 2-minute timer per target and significantly faster traces.
3.  **Target Acquisition (`scan`):** Identify your next target system (Aurora Corp, NSA, NASA, Vatican Archives) using the `scan` command with its IP address or name.
4.  **Vulnerability Exploitation (`exploit`):** Once a target is scanned, use the `exploit` command with a discovered vulnerability to gain access.
    *   *Timer Starts (Expert/Hacker):* The clock begins ticking from the moment the scan completes until the target file is downloaded!
5.  **System Navigation (`cd`, `ls`):** Inside the target server, use `cd` to change directories and `ls` to list files and directories.
6.  **Data Retrieval (`download`):** Locate the specified target file and use the `download` command to retrieve it.
    *   *Timer Stops:* Successfully downloading the target file stops the current target's timer.
7.  **Repeat:** Progress through all four initial designated targets.
8.  **The First Pursuit:** After downloading the final *initial* target's data, a trace will be initiated!
    *   **Evade (`change_proxy`, `logout`):** Use commands to lower your trace level.
    *   **Outcome 1 (Early Exit):** If you `logout` successfully here, you win Phase I, but miss the deeper challenges.
    *   **Outcome 2 (Caught):** Trace level reaches 100%.
    *   **Outcome 3 (Unlock Phase II):** If you use `change_proxy` and successfully lower your trace significantly, you evade the initial net and unlock Phase II.

### Phase II: The Deep Dive (Extended Targets)

*   **New Briefing:** Upon unlocking, you'll be briefed on the first of 10 new, extremely high-value targets, including systems like AREA_51, SWIFT, Pentagon C&C, CERN, and more.
*   **Gameplay Loop (Repeats for 10 Targets):**
    1.  **Value Assessment:** Each new target comes with a "Value" description, outlining the significance of the data you're after.
    2.  **`scan`, `exploit`, `cd`, `ls`, `download`:** The core loop continues for each of the 10 extended targets. Timers (if on Expert/Hacker) apply per target.
*   **Mid-Phase Pursuit:** After successfully compromising **5** of the extended targets, another, more intense trace will be initiated. You must evade this to continue.
*   **Final Pursuit:** After successfully compromising all **10** extended targets, the final, most challenging trace sequence begins.
*   **Ultimate Outcome:**
    *   **Ultimate Win:** Successfully download all 10 extended target files and evade the *final* trace.
    *   **Game Over (Caught):** Trace level reaches 100% during any pursuit in Phase II, or you fail to logout cleanly during the final pursuit.
    *   **Game Over (Timeout):** The timer runs out on Expert or Hacker difficulty for any of the 10 extended targets.

---

## 3. Implemented Features & Enhancements

*   **Two-Phase Gameplay:**
    *   **Phase I:** Original 4 targets.
    *   **Phase II (The Deep Dive):** An additional 10 high-stakes targets unlocked by skillful evasion of the first pursuit. Includes targets like AREA_51, SWIFT, PENTAGON_C&C, CERN_LHC_ARCHIVE, MI6_REGISTRY, GLOBAL_SATELLITE_UPLINK, THE_ILLUMINATI_GRAND_LODGE, KREMLIN_CYBER_WARFARE_DIV, DARPA_FUTURE_PROJECTS, DEEP_MIND_AI_CORE.

*   **Multi-Stage Pursuits:**
    *   **First Pursuit:** After Phase I targets. Evasion can lead to Phase II or an early win.
    *   **Mid-Phase Pursuit:** After 5 extended targets are completed.
    *   **Final Pursuit:** After all 10 extended targets are completed. Each pursuit may have slightly different characteristics or trace speeds.

*   **Difficulty System:** (Applies to both Phase I and Phase II targets)
    *   **Noob:** No timer, chill mode for exploration.
    *   **Expert:** 5-minute timer from `scan` completion to `download` for each target.
    *   **Hacker:** 2-minute timer from `scan` completion to `download` for each target, plus a faster trace during pursuit phases.

*   **Target Timers:**
    *   Visual timer display in the terminal header for Expert and Hacker modes.
    *   Timer color changes to yellow (1 minute left) and red (30 seconds left) with a flashing effect to indicate urgency.

*   **Contextual Pursuit Dynamics:**
    *   Trace level increases over time (faster on Hacker difficulty and potentially faster in later pursuits).
    *   "Messages from the other side" appear at high trace levels, simulating sysadmins closing in.
    *   Specific commands (`change_proxy`, `logout`) are crucial for survival. The `logout` command's outcome (continue, win, caught) depends on which pursuit phase you are in.

*   **Reset Command:**
    *   The `reset` command can be used at almost any time to restart the simulation from the initial difficulty selection screen, clearing all progress.

*   **Local File System & Planted Files:**
    *   Simulated local file system (`user@cyberterm`) with lore files.
    *   Each target server (original and extended) contains additional planted files for lore, jokes, or subtle clues, accessible via `cat` and `grep`.

*   **Enhanced `help` Command:**
    *   Provides more context-specific help based on the current game state.
    *   Lists newly added fun commands and easter eggs, encouraging exploration.

*   **Sound Placeholders:**
    *   Comments like `// TODO: Play sound_X.mp3` indicate where sound effects would enhance immersion.

---

## 4. Main Commands (Gameplay Progression)

These commands are essential for completing the game's objectives across both phases.

*   **`scan <target_ip_or_name>`**
    *   **Purpose:** Initiates a scan on the currently designated target system.
    *   **Output:** Reveals target information, description, (for extended targets) value assessment, vulnerabilities, and starts the timer (Expert/Hacker).
    *   **Used in:** `IDLE` state, when a `currentTarget` is set by the game flow.

*   **`exploit <vulnerability_name>`**
    *   **Purpose:** Attempts to exploit a discovered vulnerability on the scanned target.
    *   **Output:** Simulates exploit, grants access to the target server on success.
    *   **Used in:** `TARGET_FOUND` state.

*   **`ls`**
    *   **Purpose:** Lists files and directories in the current directory.
    *   **Output:** Shows directory contents. Highlights target files and special planted files.
    *   **Used in:** `INSIDE_SERVER`, `FILE_LOCATED` states (on target systems), and `IDLE` state (for the local file system).

*   **`cd <directory_name>` / `cd ..`**
    *   **Purpose:** Changes the current directory. `cd ..` moves to the parent directory.
    *   **Output:** Confirmation of directory change and new `ls` output.
    *   **Used in:** `INSIDE_SERVER`, `FILE_LOCATED` states (on target systems), and `IDLE` state (for the local file system).

*   **`download <file_name>`**
    *   **Purpose:** Downloads the specified file (primarily the target objective file).
    *   **Output:** Simulates download, displays file content, stops the target timer, and progresses the game (potentially triggering a pursuit or next target briefing).
    *   **Used in:** `INSIDE_SERVER`, `FILE_LOCATED` states.

*   **`change_proxy`** (Pursuit Phases Only)
    *   **Purpose:** Attempts to lower your trace level during a pursuit.
    *   **Output:** Simulates proxy hop, shows trace level reduction. *Critical for unlocking Phase II after the first pursuit if trace is lowered sufficiently.*
    *   **Used in:** `PURSUIT` state.

*   **`logout`** (Pursuit Phases Only)
    *   **Purpose:** Attempts to cleanly disconnect and escape the trace.
    *   **Output:** Outcome depends on the current pursuit context:
        *   **First Pursuit:** Can lead to an early Phase I win or being caught.
        *   **Mid-Phase Pursuit:** Can lead to continuing Phase II or being caught.
        *   **Final Pursuit:** Can lead to the ultimate win or being caught.
    *   **Used in:** `PURSUIT` state.

---

## 5. Utility & Fun Commands (Easter Eggs & More)

Explore the terminal with these commands for extra information, lore, or just a bit of fun!

### Information & System:

*   **`help`**
    *   **Purpose:** Displays available commands and context-sensitive help.
    *   **What:** Your primary guide to interacting with the terminal.

*   **`clear`**
    *   **Purpose:** Clears the terminal screen output.
    *   **What:** Tidies up your workspace.

*   **`reset`**
    *   **Purpose:** Resets the entire game simulation to the initial difficulty selection.
    *   **What:** Use this if you get stuck or want to start over.

*   **`whoami`**
    *   **How:** Type `whoami`.
    *   **What (Standard):** Shows your current user identity (e.g., `user (Crash_Override)` or `root`).
    *   **What (Easter Egg):** Repeated use cycles through:
        *   "A ghost in the machine."
        *   "You are... the one who knocks."
        *   If trace is high or in pursuit: "Soon to be: Inmate #655321".

*   **`history`**
    *   **How:** Type `history`.
    *   **What (Easter Egg - First Use):** Shows a fake command history from a "previous hacker's" disastrous session.
    *   **What (Subsequent Uses):** "Command history for this session would appear here. (Feature stubbed)"

*   **`man <command_name>`**
    *   **How:** `man ls`, `man exploit`, `man man`.
    *   **What (Easter Egg):** Displays stylized, humorous, or meta "manual pages" for certain commands.
        *   `man exploit`: "Point this at a hole, and hope for the best."
        *   `man man`: "The manual for the manual? That's deep, man."

### File System Interaction (Local & Target):

*   **`cat <filename>`**
    *   **Purpose:** Displays the content of a specified file.
    *   **How (Local System):**
        *   `cat README.txt`
        *   `cat my_notes/coffee_supply_status.txt`
        *   `cat tools/decoder_ring.exe`
    *   **What (Local System):** Shows content of planted files in your local simulation, like your to-do list, thoughts on coffee, or hints.
    *   **How (Target System):** After gaining access to a target server (e.g., Aurora Corp):
        *   `cd admin_stuff`
        *   `cat shadow_backup.txt`
        *   `cat internal_memos.txt`
    *   **What (Target System):** Displays content of planted files on the *target server*, revealing lore, jokes, or fake system files.
    *   **What (Target Objective):** Can also display the content of the main target file if used on it.

*   **`grep "pattern" <filename>`**
    *   **Purpose:** Searches for a specific "pattern" (text) within a specified file.
    *   **How:** Use on local or target planted files.
        *   `grep "conspiracy" internal_memos.txt` (on Aurora Corp's `/admin_stuff/`)
        *   `grep "password" shadow_backup.txt` (on Aurora Corp's `/admin_stuff/`)
        *   `grep "aliens" ufo_sightings_debunked.txt` (on NSA's `/classified/top_secret_REDACTED/`)
    *   **What:** Outputs lines containing the pattern, with the pattern highlighted.
    *   **What (Easter Egg):** Specific `grep` combinations on certain files trigger unique messages or ASCII art.
        *   `grep "conspiracy"` on `internal_memos.txt` hints at "Project Chimera".
        *   `grep "aliens"` on the NSA's UFO file shows an ASCII UFO.

### Network & Fun:

*   **`ping <destination>`**
    *   **Purpose:** Simulates sending ICMP echo requests to a host.
    *   **How (Easter Eggs):**
        *   `ping localhost` or `ping 127.0.0.1` -> "Pinging myself... still here. Lonely, though."
        *   `ping skynet` or `ping skynet.com` -> "Request timed out. (Thankfully)"
        *   `ping matrix` or `ping matrix.net` -> Shows a brief Matrix-style green character rain and a cryptic message.
    *   **How (Standard):** `ping <valid_target_ip_or_name>` -> Shows a simulated successful ping.
    *   **How (Other):** `ping <unknown_host>` -> "Request timed out. Unknown host."

*   **`sl`** (Steam Locomotive)
    *   **How:** Type `sl`.
    *   **What (Easter Egg):** An ASCII steam locomotive chugs across the screen. A classic terminal prank.

*   **`cowsay <message>` / `cowthink <message>`**
    *   **How:** `cowsay Hello World` or `cowthink Pondering my next hack...`
    *   **What (Easter Egg):** An ASCII art cow "says" or "thinks" the message you provide.

*   **`fortune`**
    *   **How:** Type `fortune`.
    *   **What (Easter Egg):** Displays a random geeky, hacker-themed, or humorous fortune.
    *   **How:** `fortune | cowsay` (pipe to `cowsay`).
    *   **What (Easter Egg):** The ASCII cow says the random fortune.

*   **`curl <url>`**
    *   **Purpose:** Simulates transferring data from a URL.
    *   **How (Easter Egg):** `curl http://<target_ip>/.hidden_api/status` (replace `<target_ip>` with an actual IP from the game's targets).
    *   **What (Easter Egg):** Returns a fake JSON response: `{ "system_status": "NOMINAL", ..., "next_hint": "Try 'decoder_ring.exe' on local system." }`
    *   **How (General):** `curl <any_other_url>` -> Simulates connection timeout or resource not found.

### Developer Parody Tools:

*   **`gcc <file.c>`**
    *   **Purpose:** Simulates compiling a C source file.
    *   **How (Easter Egg):** On Aurora Corp server, navigate to `/admin_stuff/` and type `gcc backdoor.c`.
    *   **What (Easter Egg):** Fake compilation messages for `backdoor.c`, resulting in a "highly efficient" 0-byte executable.
    *   **What (General):** `gcc somefile.c` -> Generic simulated compilation.

*   **`python <file.py>`**
    *   **Purpose:** Simulates running a Python script.
    *   **How (Easter Egg):** Type `python run_exploit.py` (anywhere).
    *   **What (Easter Egg):** Fake Python execution with a "Bobby Tables" SQL injection joke in the traceback.
    *   **What (General):** `python anotherscript.py` -> Generic simulated execution.

*   **`bash <file.sh>`**
    *   **Purpose:** Simulates running a shell script (stubbed).
    *   **What:** Generic simulated execution message.

*   **`git <subcommand>`**
    *   **Purpose:** Parody of Git version control commands.
    *   **How:** `git log`, `git push`, `git blame somefile`.
    *   **What (Easter Egg):**
        *   `git log`: Shows a humorous fake commit history.
        *   `git push`: "Push rejected. You don't have write access to this reality."
        *   `git blame somefile`: "It was probably the intern."

### System Administration Parody:

*   **`sudo <command>`**
    *   **Purpose:** Parody of the "superuser do" command.
    *   **How (Easter Egg):** `sudo make me a sandwich`.
    *   **What (Easter Egg):** "What? Make it yourself."
    *   **How (General):** `sudo <any_other_command>` (e.g., `sudo ls`).
    *   **What (General):** Prompts for a password, which always fails. States "Incorrect password. This incident WILL be reported." and may slightly increase your trace level.

*   **`chmod <permissions> <file/directory>`**
    *   **Purpose:** Simulates changing file permissions.
    *   **How:** `chmod 777 some_file` or `chmod 000 another_file`.
    *   **What:** "Permissions changed... This might have... consequences." A small chance of a "CRITICAL SYSTEM FILE CORRUPTION" message if `000` is used. May slightly increase trace.
    *   **How (Easter Egg):** If a file named `totally_not_a_virus.sh` were planted and made executable (`chmod +x totally_not_a_virus.sh`).
    *   **What (Easter Egg):** Humorous response about running a virus and a +10 trace increase. (Currently, the file isn't explicitly planted, but the `chmod +x` part on this specific name is recognized).

*   **`rm <filename_or_options>`**
    *   **Purpose:** Simulates removing files or directories.
    *   **How (Easter Egg):** `rm -rf /` or `rm -rf /*`.
    *   **What (Easter Egg):** "SYSTEM DELETION INITIATED... Just kidding. But DON'T try that on a real system... Trace level spiked!" (Significant trace increase).
    *   **How (Objective Blocker):** Attempting to `rm <target_objective_file_name>` on the target server.
    *   **What (Objective Blocker):** "ERROR: Cannot delete target objective file. Nice try, script kiddie."
    *   **What (General):** `rm somefile.txt` -> "File 'somefile.txt' removed. (Simulated, of course!)"

---

## 6. Easter Egg Quick Guide

*   **Steam Locomotive:** `sl`
*   **Sudo Sandwich:** `sudo make me a sandwich`
*   **Identity Crisis:** `whoami` (repeatedly)
*   **Ghost of Hacker Past:** `history` (first time)
*   **Ping Shenanigans:** `ping localhost`, `ping skynet`, `ping matrix`
*   **Talking Cow:** `cowsay <message>`, `fortune | cowsay`
*   **Wise Words:** `fortune`
*   **RTFM (Funny Manuals):** `man exploit`, `man man`
*   **Dangerous Permissions:** `chmod 000 some_file`
*   **Ultimate Deletion (Almost!):** `rm -rf /`
*   **Local Secrets:** `cat README.txt`, `cat my_notes/coffee_supply_status.txt`
*   **Target Server Lore:** (e.g., on Aurora) `cd admin_stuff`, then `cat internal_memos.txt`
*   **Pattern Sleuth:** `grep "conspiracy" internal_memos.txt` (Aurora), `grep "aliens" ufo_sightings_debunked.txt` (NSA)
*   **Fake Dev Work:** `gcc backdoor.c` (Aurora), `python run_exploit.py`
*   **Version Control Jokes:** `git log`, `git push`
*   **Hidden API:** `curl http://<target_ip>/.hidden_api/status`
*   **Konami Code:** Press Up, Up, Down, Down, Left, Right, Left, Right, B, A (then Enter or continue typing).
    *   **What:** "*** KONAMI CODE ACCEPTED *** ... Cheat codes enabled? Not in this simulation... +5 Style Points."

---

## 7. Future Ideas (Sound Placeholders)

The game code includes comments like `// TODO: Play sound_X.mp3`. This indicates spots where sound effects could be added in a future version to enhance immersion, such as:

*   Keyboard clicks
*   Scan/exploit process sounds
*   Success/error jingles
*   Alarms and pursuit music
*   Easter egg specific sounds (train whistle for `sl`, moo for `cowsay`, etc.)

---

Good luck, Operator Crash_Override. The fate of... well, something important... rests on your keystrokes!





AURORA_CORP_HQ_NETWORK (192.168.1.100)
Value: Access to Aurora Corp's core network could reveal sensitive R&D, unreleased product schematics, internal financial malfeasance, or evidence of their involvement in the "Global Cascade" conspiracy.
NSA_DATA_VAULT (10.20.30.40)
Value: The holy grail for intelligence. Could contain classified global surveillance data, identities of informants, details of covert operations, or even proof of extraterrestrial contact if legends are true.
NASA_RESEARCH_ARRAY (198.51.100.12)
Value: Beyond public space exploration data, this could hide schematics for experimental propulsion systems, hidden telemetry from deep space probes, or research into technologies far beyond current public understanding.
VATICAN_SECRET_ARCHIVES (207.148.192.5)
Value: Centuries of hidden history, suppressed texts, and potentially information that could reshape understanding of global power structures, ancient civilizations, or even divine mysteries.
AREA_51_PROJECT_BLUEBOOK_MAINFRAME (10.0.0.5)
Value: This implies access to decades of U.S. government secrets on UFOs, alien technology, reverse-engineered craft, and potentially even non-human biological data. The ultimate conspiracy trove.
SWIFT_INTERNATIONAL_PAYMENT_GATEWAY (172.16.0.1)
Value: Gaining control or deep access here could disrupt global finance, track illicit money flows on an unprecedented scale, or even siphon vast sums. It's the backbone of international banking communication.
PENTAGON_WAR_ROOM_C&C (10.1.1.2)
Value: Real-time global military operations, strategic plans, nuclear command (potentially).
CERN_LHC_DATA_ARCHIVE (192.0.2.55)
Value: Cutting-edge physics research, potentially data on new particles, dark matter, or even dimensional breaches if your game leans sci-fi.
MI6_AGENT_REGISTRY (172.20.5.10)
Value: Identities of covert intelligence operatives worldwide, compromising global intelligence networks.
GLOBAL_SATELLITE_UPLINK_CONTROL (203.0.113.25)
Value: Ability to control or disrupt global communications, GPS, and surveillance satellites.
THE_ILLUMINATI_GRAND_LODGE_SERVER (fd00::1234:5678:9abc:def0) (IPv6 for extra obscurity)
Value: If such a group exists in your game world, this would be their central communication and planning hub, revealing plans for global domination/manipulation.
KREMLIN_CYBER_WARFARE_DIVISION (172.31.10.20)
Value: Access to state-sponsored hacking tools, ongoing cyber operations, intelligence on foreign targets.
DARPA_FUTURE_PROJECTS_VAULT (10.5.5.5)
Value: Blueprints and research for next-generation, potentially world-altering technologies (AI, robotics, biotech, advanced weaponry).
DEEP_MIND_AI_CORE_NEXUS (192.168.200.1)
Value: Control or insight into a leading (potentially sentient or near-sentient) Artificial General Intelligence development project.                                            
                                                                         ..                                                                        
                                                                       ..-%:.                                                                      
                                                                       .+%%*.                                                                      
                                                                       .+%%*...                                                                    
                                                                   .....+%%*..-:.                                                                  
                                                                   .=*..=%%*..+#-..                                                                
                                                                 ..+%#..-%%*..*%#-.                                                                
                                                                 ..*%%:.-%%+..*%#:...                                                              
                                                               .:..+%%-.-%%+..#%*..-:..                                                            
                                                             ..=#-.=#%=.:%%+.:%%+.:##-.                                                            
                                                             .-#%=.-#%+.:%%+.:%%=.-%%=...                                                          
                                                           ...:*%*:.*%+..%%=.-%#-.=%*-.:...                                                        
                                                         ..-*-.=%#-.+%#..%%=.=%#::*%+.-#*:.                                                        
                                                         .-#%+.-#%=.=%%..#%-.+%*.-%#-.+%*:...                                                      
                                                     ......+%#-.+%*:-#%:.#%-.+%*.=%*.-#%=.=-...                                                    
                                                     ..:*+.:*%+.-#%:.#%-.#%-.*%=:*%=.+%+:-#%-..                                                    
                                                     ..=%%=.=%#-.*%=.*%=.#%=.##-:##--##-:*%+.:...                                                  
                                                   ..-..+%#-.+%+:=%*:+%+.*%-.%#:-%*.+%+.+%*::##:.                                                  
                                                   .+%*::+%*:-#%-:#%--%#.*%-:%#.+#=-##--##-:*%*...                                                 
                                                  ..-#%#::*%*:=%*:+%+:#%.+%=-%*:##-=%+:*%=:*%*:-#+..                                               
                                                .-#+.:#%#--#%+:*%=-##:#%:+%==%+-%+:#*-+%+:*%*:=%%*..                                               
                                                .+%%*::*%#--#%==##-*%-+%=+%=+%=+#==%=-#*-+%*:=%%=.=#-.                                             
                                              .+:.:#%%-:+%#==%#=*%++%*+%++%=*%=##=#*=*#-+%*:+%#-:*%%+.                                             
                                            ..*%%*:.+%%*-+%%++%#+#%+#%+%#*%+#%=%*+%++%=+%+-*%*:=%%*::++.                                           
                                          .....=%%%*:=%%%+*%%*#%%%%%%%#%%#%#%%#%#%#+%*+%*-#%+:*%%-.=%%%=                                           
                                          .+%%+..+%%%#=#%%%%%%##%+*#-##=%:%-%*#%#%#%#*%*+#%==%%+.=%%%+.:=-..                                       
                                        ...-#%%%%=:#%%%%%%%#+#*-=*-+-:***.%=%+#+%#*#*%##%#=*%*:=%%%-.-#%%#-.                                       
                                      ..-*+:..*%%%%%#%%%#--*#+++:-==--+=#-#:#-#+**#*#**%*#%%++%%#:.*%%%#:..:..                                     
                                      .-#%%%%#+-=%%%%%+:+#=-:+**%+**+**###%#%####%##**%*#%**%%%-=#%%%=.:+#%%*:                                     
                                    .....:=#%%%%%%%%*%#--=*%#+###%%%%%%%%%%%%%%%%%%%%%#%#*#%*+#%%%+:-*#%%%#=:...                                   
                                  ..:*%%##+=-=#%%%%%*+--+##*#%%%%%%###%%%%%%%%%%%%%#*#%%%%###%%*+*#%%%#+:..-+##=..                                 
                                  ..:+*%%%%%%%%%%*-:=*%#*#%%%%%%#**%%%%%%%%####%%%%%*+***%%%%##%%%%*===+*#%%%%#+:.                                 
                                ..:-:...:-=*%%%%%#+++%#%%%%%%##++#%*=::-+########%%%%#+**+#%%%%#***#%%%%%#+=:.......                               
                              ...+%%%%%%##***#%=:-=*%%%%%%%#**=-#%+:....=%%%%%%%#***%%*+***#*%%%%%%%*+=---==+*##%%#-..                             
                              ..:=+***##%%%%%%%%%%%%%%%%##**+-:+%#-.....*%%%%%%%%*+*#%#++*###*++%####%%%%%%%%%%##**=..                             
                            ...........:::-+#*=+#%%%%%####*=::-*%#=...:+%%%%%%%%%#+=+%%*==+#%%%%########*=-:............                           
                          ...=%%%%%%%%%%%%%%%%%%%%%%%%#====:..-#%#+++*%%%%%%%%%%%*+**%%*==--=+++++*#%%%%%%%######%%%%%*...                         
                          ..=%#################%#%#+-=:.......:*%#+++*%%%%%%%%%%#+==+%%+==+++*#%###%%%%%%%%%%%%%%%%%%%%#:.                         
                         ...............:--=*%%%%%%#=**.-=:....+%%*+++#%%%%%%%%%*+=*%%*--+#%%%%%%%%%%%#*=:................                         
                         .:-=+*#%%%%%%%%%%%%%##**+....-==++-...=#%%++=+*#%%%%#++++*#%%+-=#%%#*+-=+#%%%%%%%%%%%%%*+=--:..                           
                       .=%%%%%%%%%%#*+=-:....:+###%%#=-:::--:..:-#%%**++*******+*#%%##+=*##+=*%%%%%%%#:.::=+*##%%%%%%%%%%%%*.                      
                     ..*%%*+=::.... ..-=*##%%%**+--=*#+=+:--::.::-*%%%#*****###%%%%#+*=+#*+*%%%%=-=*%%%%##+-:. ...::=+#%%%%%#:.                    
                     ...... ..:-+*##%%%%#+=::..-*#%%+----==-==:....:*%%%%%%%%%%%##++**###+*%*=-*%%#*=::-+*%%%%#*+-:.   ...::-=:                    
                       .-=*##%%%%%%*=-:..:-+##%*=-:=*#*=:-++-:--=-.::---+==*=+*=+===+=*++##++#%#+-=#%%#*=:.:-=*%%%%%##*=:..                        
                 ..=*#%%%%%%%#*=-:...-+*#%%*=-.:=*%#==+***=++--=-=+-=-+==:-+:=-=-==*=++*#*+##+=+%%#+--+#%%#+=:..:-+*%%%%%%#*+=-..                  
                 .*%%%%%#+=-. ..:=+#%%%*=-..-+#%*=:-+##=:+**+#*+#***=*=*+*-#*#=*++*###%#*#%++#%#==*%%#+-:=*#%%#+=:...:-+#%%%%%%%#*:                
               .:*%#+=:.. ..-=*%%%%*+-..:=*%%*-.:=#%*--*#+-+*=-*+=*+##*%*%=%###*%*#**#+*#++#%+=#%%+-=*%%#=:.:=*%%%#+-:.. .:=*#%%%%#=.              
               :-:.. ..:-+#%%%%#+-...-+#%%*=..-*%#=.-*%*-=#*-=#+-+-=#-##=%-#*-#+*==#++%++##=+%%=-*%%*::=#%%#=:..-*#%%%%+-:. ...-*#%%+..            
                 ..:-*%%%%%#*=...:-*%%%*=..:*%%*:.-#%*:-##=:*#==#+=#*-#--#:##:%*=#++%++%*=#%+-*%%-.+#%#-.:+#%%#=:..:+#%%%%%+-..   .:+=.            
             ..:=*%%%%%%#=. ..:+#%%%*-..:+%%#=..=%%*.:*%*:=#*:=#+:*#:*%:*%.#%:##-*#=*%==##-+%%-:*%%-.-#%%+:.:+#%%#=:...=#%%%%%#+:..                
         ...-*%%%%%%%*-. ..:*%%%%#=...=#%%*:..+%%*..+%#-.+%*:=%+:+%--#*.#%.*%-=%=-%*-*%--#%-:#%*.:#%%-.:#%%*:..-*%%%#=....:#%%%%%%#=...            
         .-#%%%%%#=. ...-#%%%%#-...-#%%%=..:#%%+..=%%+.-#%=.=%+:=%+.*%-:%#.+%=:%*:+%=:#%-:#%=.+%%=.:%%#-..+%%#=...=#%%%#-.. .:*%%%%%%%*:...        
       ..=%%%%*:.....=#%%%%#-...:*%%%*:..=#%%=..=%%*..+%#-:+%*:-##:-##.-%*.+%+:*#=:##--#%-.*%*::#%%:.-%%#-..=%%%*:..:+%%%%#-.....=%%%%%%%#=..      
     ..:+%#+:....:=#%%%%#=:...=#%%%+:..=#%%=..=#%#:.-#%*::*%*::#%-.*%+.+%*.=%*.=%*.=%*:-#%-.+%%-.-%%*..=%%#-..=#%%#-...-#%%%%#-....:=#%%%%%*:..    
     ...::.... ..:::::::.....:::::....::::....:::...:::...::...::..::..:::..::..::..::..:::..:::...:::...:::....::::.. ..:::::::. ....:::::::..    
