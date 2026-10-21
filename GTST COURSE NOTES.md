#Metadata
#course
Geez Tech Security Tester (GTST)
#source
GTST - Introduction.pdf
#tags
GTSTcybersecurityethical-hackinggitmarkdown
#title
GTST --- Introduction to Ethical Hacking
#type
study-notes

# GTST --- Introduction to Ethical Hacking

> !info!info About these notes These notes are organized from the GTST  
> Introduction PDF. They follow the instructor's topics and add simple  
> explanations to make revision easier. Where a practical action affects  
> a real system, only test systems you own or have explicit permission  
> to assess.

## ##Table of contents

- \[#1. Course overview]
- \[#2. Mindset and requirements]
- \[#3. Git, GitHub, Markdown and Obsidian]
- \[#4. Introduction to hacking]
- \[#5. Types of hackers]
- \[#6. Why learn ethical hacking?]
- \[#7. Why attacks happen]
- \[#8. Information security and the CIA triad]
- \[#9. Skills needed]
- \[#10. Phases of hacking]
- \[#11. Penetration testing]
- \[#12. Penetration-testing types]
- \[#13. Cybersecurity ethics]
- \[#14. Career opportunities]
- \[#15. Important vocabulary]
- \[#16. Quick revision questions]
- \[#17. Practical checklist]

---

## 1. Course overview

The PDF divides the course into two seasons.

### #Season 1 --- Foundations

- Introduction to ethical hacking
- Linux
- Python
- Bash
- Networking

### #Season 2 --- Security topics

- Footprinting and reconnaissance
- Network scanning
- Malware threats
- Social engineering
- Steganography and cryptography
- Sniffing
- System hacking concepts
- DoS/DDoS and the dark web
- Website security
- Wireless-network security
- Capture the Flag (CTF)
- Bug bounty hunting and next steps

> !tip!tip Learning order Build the foundations first: computer basics,  
> Linux, networking, and programming. Security tools make much more  
> sense when you understand what they are doing.

## 2. Mindset and requirements

The instructor emphasizes that hacking is not simply breaking into  
social-media accounts and that becoming skilled takes time.

### Core mindset

- **Ethics:** use technical skills responsibly.
- **Discipline:** study and practise consistently instead of relying  
    only on motivation.
- **Passion and curiosity:** ask how systems work and why they fail.
- **Patience:** do not expect to become an expert overnight.
- **Simplification:** break difficult concepts into small,  
    understandable parts.
- **Attention to detail:** something that looks unimportant now may  
    become useful later.
- **Active learning:** ask questions, complete exercises, and  
    participate.

### What you need

- A computer
- Internet access when available
- Consistent practice
- Effective note-taking
- A habit of asking questions and documenting what you learn

**Afaan Oromoo:** Ogummaa cybersecurity barachuuf kaka'umsa qofa osoo  
hin taane, naamusa, obsaa, shaakala yeroo yeroon godhamu fi gaaffii  
gaafachuun barbaachisaadha. Sirna nama biraa hayyama malee qorachuun  
ethical hacking miti.

---

## 3. Git, GitHub, Markdown and Obsidian

### 3.1 Git

**Git** is a version-control system. It records changes to files so you  
can review previous versions and track your work.

- A repository (repo) is a project folder tracked by Git.
- A commit is a saved checkpoint of changes.
- Git can work locally without an internet connection.
- Remote hosting services can store a copy of a repository online.

### 3.2 GitHub

**GitHub** is an online platform that hosts Git repositories and  
supports collaboration.

**Remember the difference:**

- **Git** = the version-control tool.
- **GitHub** = an online service where Git repositories can be hosted.

### 3.3 Markdown

**Markdown** is a lightweight way to format plain-text notes using  
symbols.

``# Main heading ## Subheading **Bold text** *Italic text* - First item - Second item 1. First step 2. Second step `inline code` > A quotation or important reminder``

The instructor's exercise uses a file called Day1_Introduction.md and  
a README.md.

### 3.4 Obsidian

**Obsidian** is a note-taking application that stores notes as Markdown  
files. It helps organize notes into folders and connect related  
concepts.

Suggested GTST vault structure:

`GTST/ ├── README.md ├── 00 - Course Overview/ │ └── Course Roadmap.md ├── 01 - Introduction/ │ └── Day1 - Ethical Hacking.md ├── 02 - Linux/ ├── 03 - Networking/ ├── 04 - Python/ ├── 05 - Bash/ ├── 06 - Reconnaissance/ ├── 07 - Scanning/ ├── 08 - Web Security/ ├── 09 - Cryptography/ ├── 10 - CTF and Bug Bounty/ └── Labs and Practice/`

You can adjust the folders as the course progresses. Do not create empty  
folders just for appearance---use them when you have notes to put there.

### 3.5 Basic Git workflow

Run these commands inside your project folder.

**First-time setup**

`git config --global user.name "Your Name" git config --global user.email "you@example.com" git init`

git init initializes a Git repository in the current folder.

**Everyday workflow**

`git status git add . git commit -m "Add GTST introduction notes" git log`

---

Command Meaning

---

git status Shows changed and untracked files

git add . Stages changes in the current  
folder

git commit -m "message" Saves a checkpoint of staged  
changes

git log Shows commit history

git clone <repository-URL> Copies a remote repository to your  
computer

---

**Important:** git add . stages changes; it does not itself save a  
commit. git commit creates the checkpoint.

### 3.6 Connecting a local repository to GitHub

The PDF demonstrates creating a repository on GitHub, adding its URL as  
a remote, and pushing commits.

`git remote add origin <repository-URL> git push -u origin main`

Some older repositories use master instead of main. Use the branch  
name that actually exists in your repository.

To download an existing repository:

`git clone <repository-URL>`

### 3.7 GitHub authentication and tokens

The PDF shows using a GitHub token for authentication. Treat tokens like  
passwords.

- Never paste a token into public notes or a public repository.
- Do not commit tokens, passwords, private keys, or other secrets.
- Store credentials using a trusted credential manager.
- If a token is exposed, revoke it and create a replacement.

### 3.8 GitHub Desktop workflow

The PDF also demonstrates a graphical alternative:

1. Create a repository and choose its name and local location.
2. Sign in to GitHub.
3. Open or edit the repository's Markdown notes in Obsidian or VS Code.
4. Review detected changes in GitHub Desktop.
5. Enter a meaningful commit summary.
6. Commit the changes.
7. Push the commit to GitHub.

**Git is local version history; pushing sends commits to the remote  
repository.** A commit is not automatically uploaded.

### 3.9 Instructor's first exercise

- Create a local repository named gtst_course.
- Create Day1_Introduction.md and README.md.
- In Day1_Introduction.md, add:

`# DAY1: ETHICAL HACKING Hello **this** is test`

- In README.md, add:

`This is note written while taking the Geez Tech Security Tester course.`

- Commit the files and push the repository to GitHub.

Useful links from the PDF:

- [Obsidian](https://obsidian.md/)
- [Git for Windows](https://gitforwindows.org/)
- [Markdown Guide --- Cheat  
    Sheet](https://www.markdownguide.org/cheat-sheet/)
- [GitHub](https://github.com/)

---

## 4. Introduction to hacking

### 4.1 What is hacking?

The course describes hacking as exploiting weaknesses in systems or  
security controls to gain access. In security work, the key distinction  
is whether the activity is authorized and ethical.

### 4.2 What is ethical hacking?

**Ethical hacking** is the authorized examination of computers,  
applications, or networks to find weaknesses and report them to the  
responsible organization so they can be fixed.

An ethical hacker aims to help the owner improve security---not to steal  
information, damage systems, or access accounts without permission.

### 4.3 What is a hacker?

A **hacker** is a person who uses technical knowledge to understand,  
test, or manipulate how systems work. The term alone does not tell you  
whether the person's actions are ethical; authorization, intent, and  
conduct matter.

**Afaan Oromoo:** Ethical hacking jechuun sirna kompiitaraa, application  
ykn network tokko hayyama qabaachuun hanqina nageenyaa isaa qorachuu,  
ragaa galmeessuu fi abbaa sirna sanaaf gabaasuu dha.

---

## 5. Types of hackers

The PDF classifies hackers by ethics and by skill. These are separate  
ways of classifying someone.

### 5.1 Based on ethics

---

Type Meaning in the course

---

**White hat** Works ethically and with  
authorization to help improve  
security

**Black hat** Uses hacking skills for malicious  
or unauthorized purposes

**Grey hat** Falls between the two in the  
course's simplified classification;  
may find weaknesses without proper  
authorization

---

> !warning!warning Important distinction Finding a vulnerability does not  
> automatically give someone permission to test, access, or change the  
> affected system. A person who means well can still cross legal and  
> ethical boundaries.

### 5.2 Based on skill or experience

---

Term Meaning in the PDF

---

**Newbie / Noob** Beginner with little or no hacking  
knowledge

**Script kiddie** Relies on tools or scripts made by  
others, often without deeply  
understanding them

**Hacker** The PDF's middle skill category; a  
person with developing skill and  
limited experience

**Elite / Pro hacker** The PDF's label for a highly  
skilled and experienced person

---

These labels are informal. Real competence is better judged by  
understanding, careful testing, problem-solving, documentation, and  
responsible conduct---not by a label.

---

## 6. Why learn ethical hacking?

The PDF lists these goals:

1. Prevent unauthorized access.
2. Discover vulnerabilities.
3. Strengthen an organization's security.
4. Protect data.
5. Reduce the risk of security breaches.
6. Improve security awareness.
7. Create career opportunities and earn money through legitimate  
    security work.

The central goal is to discover and help fix weaknesses before they are  
abused.

### Who can become an ethical hacker?

The course highlights:

- Knowledge of technology and security
- Ability and willingness to learn
- Strong work ethics
- Background or interest in forensics and security

You do not need to know everything before beginning. You do need to  
build the fundamentals and practise consistently.

---

## 7. Why attacks happen

The PDF gives this model:

> **Attack = Motive (goal) + Method + Vulnerability**

This is a learning model, not a complete formula for every real-world  
incident.

### 7.1 Motive

Possible motives listed in the PDF include:

- Information theft
- Manipulating data
- Financial loss or financial gain
- Revenge
- Ransom
- Damaging an organization's reputation

### 7.2 Method

The **method** is the approach used to attempt an attack. The course  
studies different methods in later topics.

### 7.3 Vulnerability

A **vulnerability** is a weakness in software, hardware, configuration,  
processes, or human practice that could be exploited.

### Example

A web application has an unpatched weakness (**vulnerability**). Someone  
wants to steal customer information (**motive**) and tries to exploit  
that weakness using a particular technique (**method**).

**Defender's question:** What weakness exists, what evidence shows it,  
what could the impact be, and how can the owner reduce the risk?

---

## 8. Information security and the CIA triad

The PDF introduces the **CIA triad**, three foundational goals of  
information security.

### 8.1 Confidentiality

Information should only be accessible to authorized people or systems.

- Example: access controls prevent an unauthorized user from reading  
    private student records.
- Afaan Oromoo: **Iccitii eeguu** --- odeeffannoon namoota hayyama  
    qaban qofa bira ga'uu qaba.

### 8.2 Integrity

Information should remain accurate, complete, and protected from  
unauthorized changes.

- Example: only authorized staff can change a student's official  
    grade, and changes can be audited.
- Afaan Oromoo: **Sirrii fi guutuu ta'uu** --- odeeffannoon hayyama  
    malee jijjiiramuu ykn manca'uu hin qabu.

### 8.3 Availability

Information and systems should be accessible to authorized users when  
needed.

- Example: maintaining reliable services and backups so users can  
    access a system when required.
- Afaan Oromoo: **Argamummaa** --- sirni fi odeeffannoon yeroo  
    barbaachisutti namoota hayyama qabanif argamuu qaba.

### Memory aid

- **C --- Confidentiality:** Who can see it?
- **I --- Integrity:** Can I trust that it has not been changed  
    improperly?
- **A --- Availability:** Can authorized users access it when needed?

Security controls often support more than one of these goals.

---

## 9. Skills needed

The PDF names four core areas:

### 9.1 Programming

Programming helps you understand application logic, automate repetitive  
tasks, read code, and recognize coding mistakes. Python is included in  
the course roadmap.

### 9.2 Networking

Networking helps you understand how devices communicate, including IP  
addresses, ports, protocols, routing, and DNS.

### 9.3 Linux

Linux knowledge helps you navigate a terminal, manage files and  
permissions, run tools, inspect processes, and understand system  
behavior.

### 9.4 System administration

System administration helps you understand users, permissions, services,  
logs, configuration, updates, and how systems are maintained.

**Study principle:** Do not only memorize tool commands. Learn what the  
command does, what output it produces, and what that output means.

---

## 10. Phases of hacking

The PDF lists five phases:

1. Reconnaissance
2. Scanning
3. Gaining access
4. Maintaining access
5. Clearing tracks or logs

These are a simplified, traditional attack lifecycle presented for  
learning. Real incidents do not always follow these phases in a neat  
order.

### 10.1 Reconnaissance

Gather information about a target.

**Defensive understanding:** Know what assets your organization exposes  
and which information is publicly available.

### 10.2 Scanning

Examine systems or services to identify reachable hosts, open ports, or  
potential weaknesses.

**Defensive understanding:** Inventory services, verify that exposed  
services are necessary, and investigate unexpected exposure.

### 10.3 Gaining access

An attacker attempts to exploit a weakness or misuse credentials to  
obtain access.

**Defensive understanding:** Patch vulnerabilities, enforce strong  
authentication, limit privileges, and monitor suspicious activity.

### 10.4 Maintaining access

In an attack scenario, this refers to attempts to retain access over  
time.

**Defensive understanding:** Review accounts, persistence mechanisms,  
startup items, scheduled tasks, and logs when investigating suspicious  
activity.

### 10.5 Clearing tracks or logs

The PDF includes this as a phase describing attempts to hide activity.

**Defensive understanding:** Protect logs from tampering, centralize  
important records, restrict log access, and monitor for gaps or  
suspicious deletions.

> !important!important Ethical boundary Learn these phases to understand  
> attacks and strengthen defenses. Do not attempt to access or persist  
> in systems you do not own or have explicit permission to test, and  
> never erase another system's logs.

---

## 11. Penetration testing

### 11.1 Definition

**Penetration testing (pentesting)** is an authorized security  
assessment that simulates selected attacker techniques to find and  
validate security weaknesses.

The PDF highlights three outcomes:

- Find vulnerabilities
- Assess security measures
- Document results and prepare a report

### 11.2 Why is penetration testing needed?

According to the PDF:

- Identify threats.
- Evaluate security protections and controls.
- Assess an organization's security.
- Evaluate network security.
- Help guide infrastructure improvements.

### 11.3 What makes a test professional?

A useful assessment needs:

1. **Permission and scope:** written authorization, approved targets,  
    and clear boundaries.
2. **Planning:** define objectives, timing, limits, and contacts.
3. **Controlled testing:** minimize disruption and protect data.
4. **Evidence:** record relevant observations and reproducible  
    findings.
5. **Risk assessment:** explain likely impact and severity.
6. **Reporting:** describe findings, evidence, and recommended fixes.
7. **Retesting:** where agreed, check whether fixes worked.

The last list is a practical study framework; the PDF specifically  
emphasizes finding vulnerabilities, security measures, and  
documentation/report preparation.

---

## 12. Penetration-testing types

The PDF distinguishes tests by how much information the tester has at  
the start.

---

Type Starting knowledge Analogy in the PDF

---

**Black box** Little or no prior Test from an outsider's  
internal knowledge perspective

**White box** Extensive information Test with a  
about the system developer-like level of  
knowledge

**Grey box** Limited or partial Test with a regular  
information user's level of  
knowledge

---

### Black-box testing

The tester begins with little information about the internal design.  
This can help assess what an outside tester could discover within the  
agreed scope.

### White-box testing

The tester has substantial internal information, such as architecture or  
source-code access. This can help investigate deeper design and  
implementation issues.

### Grey-box testing

The tester has some information or ordinary user access, but not full  
internal knowledge. This can model a limited-access scenario.

**Remember:** The main difference is the amount of information available  
to the tester---not whether the test is ethical. All three can be  
authorized.

---

## 13. Cybersecurity ethics

The PDF stresses that ethics is central to ethical hacking and that  
permission is essential.

### Rules to follow

- Obtain explicit authorization before testing.
- Stay within the agreed scope.
- Do not access, copy, expose, modify, or delete data without  
    authorization.
- Avoid disrupting services or harming users.
- Protect any sensitive information encountered.
- Keep accurate notes and evidence.
- Report findings responsibly to the authorized contact.
- Use practice labs, CTFs, or systems you own for exercises.

The PDF mentions Ethiopia's Computer Crime Proclamation, written in  
Amharic as **የኮምፒዩተር ወንጀል አዋጅ**. These notes do not interpret the law or  
provide legal advice; check authoritative, current legal sources for  
legal questions.

> !danger!danger Permission first Curiosity is not authorization. A public  
> website, Wi-Fi network, social-media account, or server is not  
> automatically available for security testing just because you can  
> reach it.

**Afaan Oromoo:** Hayyama qabaachuun murteessaadha. Website ykn network  
nama biraa irratti qorannoo gochuun, yaadni kee gaarii ta'ullee, hayyama  
ifa ta'e malee sirrii miti. Shaakalaaf lab ofii keetii ykn CTF  
fayyadami.

---

## 14. Career opportunities

The PDF lists these possible roles:

- Cybersecurity expert
- Security analyst
- Cybersecurity consultant
- Web penetration tester
- Internal or external penetration tester
- Network security tester
- Bug bounty hunter

These roles require different levels of knowledge and experience. Build  
foundational skills, complete legal practice labs, document your work,  
and learn to explain findings clearly.

### A beginner's progression

1. Learn computer, operating-system, and networking fundamentals.
2. Practise Linux and basic scripting.
3. Learn how web applications and authentication work.
4. Use legal labs and beginner CTF challenges.
5. Keep clear notes of what you tried, observed, and learned.
6. Practise writing a short report with evidence and remediation.
7. Build a portfolio that contains only work you are allowed to share.

---

## 15. Important vocabulary

---

Term Simple definition

---

**Ethical hacking** Authorized security testing to find  
and report weaknesses

**Hacker** A person who uses technical skills  
to understand or manipulate systems

**Vulnerability** A weakness that could affect  
security

**Exploit** A technique or code that takes  
advantage of a vulnerability

**Motive** The goal or reason behind an action

**Reconnaissance** Gathering information about a  
target

**Scanning** Checking systems or services for  
information such as reachability  
and exposure

**Penetration test** An authorized assessment that  
simulates selected attack  
techniques

**CIA triad** Confidentiality, Integrity, and  
Availability

**Git** A version-control system

**GitHub** An online platform for hosting and  
collaborating on Git repositories

**Repository** A project location tracked by Git

**Commit** A recorded checkpoint of staged  
changes

**Markdown** Plain-text formatting syntax

**Obsidian** A note-taking app that uses  
Markdown files

**CTF** Capture the Flag; a structured  
cybersecurity challenge

**Bug bounty** A program that rewards eligible  
vulnerability reports under defined  
rules

---

---

## 16. Quick revision questions

Try answering these without looking at the notes. Write your answers  
under each question, then check the sections above.

1. What is the difference between hacking and ethical hacking?
2. What is the difference between Git and GitHub?
3. What does a Git repository contain or track?
4. What do git status, git add, git commit, and git log do?
5. Why must you protect a GitHub token?
6. Name the three hacker types classified by ethics in the PDF.
7. What is a script kiddie?
8. Give three reasons for learning ethical hacking.
9. Explain the course's model:  
    Attack = Motive + Method + Vulnerability.
10. What does each letter in the CIA triad stand for?
11. Name the four foundational skill areas listed in the PDF.
12. List the five phases of hacking shown in the PDF.
13. What are the main purposes of penetration testing?
14. Compare black-box, white-box, and grey-box testing.
15. Why is explicit permission necessary before testing a system?
16. Name four career paths listed in the PDF.

### Self-assessment

- I can explain the main concepts without memorizing the exact  
    wording.
- I can describe the CIA triad and give an example for each part.
- I can explain the basic Git workflow.
- I can distinguish the three penetration-testing types.
- I understand that security testing requires authorization.
- I completed the instructor's repository exercise.

---

## 17. Practical checklist

### Obsidian notes

- Create a GTST vault or course folder.
- Save this note as Day1 - Introduction to Ethical Hacking.md.
- Use clear headings and meaningful file names.
- Add new notes as you complete each course topic.
- Link related notes with Obsidian links, for example  
    [[Linux Fundamentals]].

### Git and GitHub

- Install Git and configure your name and email.
- Initialize a repository for course notes.
- Check changes with git status.
- Stage and commit changes with a meaningful message.
- Connect to your own GitHub repository and push.
- Confirm that the files appear on GitHub.
- Keep tokens and other secrets out of notes and commits.

### Ethical practice

- Use only authorized targets.
- Understand the lab rules and scope before testing.
- Record what you learn and what evidence supports it.
- Explain the risk and how to fix the issue.
- Never mistake access for permission.