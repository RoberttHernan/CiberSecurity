# Personal Code of Conduct for Ethical Hacking

Nov 22, 2026 · @Robert

## 1. Purpose and scope

I commit to using offensive security skills only to protect people and systems, never to harm them, and only where I hold explicit permission. This code turns that commitment into rules I can check before every action.

**It applies to me in every role I hold:**

- Systems engineering student at USAC (coursework, labs, CTFs, thesis work)
- Workforce Management and data analyst professional at my employer
- Independent software developer working with client code, cloud accounts and data
- Candidate for security certifications (CompTIA Security+ and later cloud security tracks)
- Instructor creating security training content, including my Wireshark course for Udemy

**It covers these activities:** network scanning and enumeration (nmap and similar), packet capture and traffic analysis (Wireshark, tcpdump), vulnerability assessment, penetration testing, password auditing, social engineering tests, cloud and container security reviews (AWS, GCP, Azure, Docker, Kubernetes), malware analysis in isolated labs, and publishing or teaching any of the above.

**Core rule:** if I am unsure whether something is allowed, I treat it as not allowed until I have written confirmation.

## 2. Guiding principles

My principles follow the order of precedence used by the [ISC2 Code of Ethics](https://www.isc2.org/ethics): when two principles conflict, the higher one wins. I add commitments drawn from the [EC-Council Code of Ethics](https://www.eccouncil.org/code-of-ethics/), which binds every CEH candidate and certified member.

1. **Protect society and infrastructure first.** No engagement, client or grade justifies harming the public, critical services or innocent third parties.
2. **Act honorably, honestly, justly, responsibly and legally.** I tell the truth about what I found, what I did and what I broke.
3. **Give diligent, competent service to those who authorize me.** I only take work I am qualified to do, and I say so when I am not.
4. **Advance and protect the profession.** I share knowledge responsibly, mentor others and never give "hacker" work a criminal reputation.
5. **Least harm, least access.** I use the least intrusive technique that answers the question, and I touch only the data the test requires.
6. **Confidentiality by default.** What I learn about a client, employer or classmate stays private unless they consent or the law requires disclosure (EC-Council).
7. **Respect intellectual property.** I rely on my own work, credit others, and do not pirate tools, courses or exam material (EC-Council).
8. **No conflicts of interest.** I disclose any relationship that could bias my findings or recommendations.

## 3. Authorization and scope

No written authorization, no test. A verbal "go ahead", a friend's permission or a system being "publicly reachable" is never authorization.

**I will:**

- Get signed permission from the system's legal owner, not just a user or employee, before any scan or test.
- Confirm in writing the scope (IPs, domains, apps, cloud accounts), the testing window, allowed techniques, and an emergency contact.
- Check cloud provider rules before testing anything hosted there (AWS, GCP and Azure each publish penetration testing policies).
- Stop immediately and notify the contact if I hit something outside scope, cause an outage, or find evidence of a real attacker.
- Treat third-party services (SaaS, CDNs, payment processors) as out of scope unless their owner also authorizes.

**I will not:**

- Scan, probe or log into networks I do not own or am not authorized to test, including my employer's, my university's, public Wi-Fi, or neighbors' networks.
- Use my work access, credentials or VPN to test anything outside my job duties, even out of curiosity.
- Run denial-of-service, destructive payloads or data exfiltration unless the scope explicitly allows it.
- Keep persistence, backdoors or accounts after the engagement ends.

## 4. Data handling, confidentiality and privacy

Any data I see during a test belongs to its owner, and I handle it as if it were the most sensitive data they have.

| Situation | My rule |
| --- | --- |
| Personal data found (names, IDs, emails, health, payroll) | View only what proves the finding, never copy it in bulk, redact it in reports |
| Credentials or keys recovered | Use only inside scope, report them, never reuse them elsewhere or keep them |
| Packet captures (pcap) | Capture only scoped interfaces, store encrypted, delete when the engagement closes |
| Client or employer data at work | Use only for my job duties, never in personal labs, courses or posts |
| Evidence and reports | Encrypted at rest, shared only with named contacts, retained only as long as agreed |
| Course and demo material | Built from my own lab data, with real IPs, names and hosts removed |

I will not collect, give, sell or transfer personal information to a third party without the owner's prior consent, as the EC-Council code also requires.

## 5. Lab, tools and personal environment

I practice offensive techniques only in environments I own or that are built for practice.

- **Approved practice targets:** my own VMs and containers, an isolated home lab VLAN, deliberately vulnerable apps (DVWA, Juice Shop, Metasploitable), and platforms whose terms allow it (Hack The Box, TryHackMe, PortSwigger Academy, official CTFs).
- **Home network:** I scan only devices I own. Devices of family or guests on the same network need their owner's consent first.
- **Isolation:** malware samples and exploits run only in isolated VMs with no shared folders and no route to production, work or university networks.
- **Cloud labs:** separate personal accounts with budget alerts, never my employer's or a client's accounts, and torn down when finished.
- **Tools:** I download tools only from official sources, verify hashes when published, and never use cracked or pirated software.
- **Work devices:** I never install offensive tools on employer-owned devices unless my role and IT policy allow it.
- **Code I write:** proof-of-concept code stays in private repositories until any related vulnerability is fixed, and I never publish ready-to-use malware.

## 6. Responsible disclosure

When I find a vulnerability, the owner hears about it before anyone else, and I never use it for leverage or profit outside an agreed bug bounty.

1. Stop testing as soon as the issue is confirmed; do not dig deeper to "prove" impact on real data.
2. Look for the owner's official channel: a `security.txt` file, a vulnerability disclosure policy, or a bug bounty program.
3. Report privately with clear steps to reproduce, impact, and a suggested fix.
4. Give a reasonable time to fix it before any public mention; 90 days is a common industry default.
5. Publish only after a fix, or with the owner's agreement, and without exploit code that would harm unpatched users.
6. If I found it by accident on a system I was not authorized to test, I report it without further testing and say plainly how I came across it.

I never demand payment in exchange for not disclosing. That is extortion, not research.

## 7. Workplace, academic and teaching commitments

Each role I hold gives me a different kind of access, and each comes with its own limits.

**At work (Current**** and any future employer)**

- Follow the employer's acceptable use and information security policies, which override this code where they are stricter.
- Report security weaknesses I notice through the official channel (IT or security team), never test them myself.
- Keep scheduling, real-time and analytics data (agent records, client metrics) inside approved systems.

**At USAC and in coursework**

- Attack only the targets the professor or lab guide defines; university networks and portals are off limits.
- Do my own work on graded labs and certification exams, and never share or use leaked exam questions ("braindumps").
- Help classmates learn the technique, not hand them answers or tools to misuse.

**As an independent developer**

- Put security testing of client systems in the contract, with scope and liability terms, before I start.
- Disclose any security weakness I find in client code honestly, even when it came from my own work.

**As an instructor**

- Open every offensive lesson with a legal and ethical warning and the authorization rule.
- Demonstrate only in my own lab, with no real third-party targets on screen.
- Teach detection and defense alongside each attack technique.
- Refuse to give students one-on-one help attacking systems they cannot show they own.

## 8. Legal framework

Good intentions are not a legal defense, so I follow the law of every country where a target system, its data or its owner sits. This section is a personal reference, not legal advice.

**Guatemala.** The Código Penal (Decreto 17-73), articles 274 "A" to 274 "H", already criminalizes destroying computer records, altering programs, prohibited records, manipulating information, using information, destructive programs and maliciously altering an origin number ([article list](https://www.conceptosjuridicos.com/gt/articulos/codigo-penal-articulo-274/)). Congress is reviewing initiative 6347, which would add offenses such as illicit access to systems, with prison terms of three to six years, and attacks on systems of up to nine years ([Infobae, July 2026](https://www.infobae.com/guatemala/2026/07/24/guatemala-propone-castigar-con-hasta-nueve-anos-de-carcel-a-quienes-cometan-delitos-ciberneticos/); [La Hora](https://lahora.gt/?p=955474)). I will re-check its status whenever I review this code.

**Abroad.** Clients, employers and cloud providers are often in the United States, Canada or Europe, where laws such as the U.S. Computer Fraud and Abuse Act and data protection rules like the GDPR can apply to me even while I work from Guatemala.

**Contracts.** NDAs, statements of work, bug bounty terms and platform terms of service are binding on me too; breaking them can be a legal problem even when no crime occurs.

**When in doubt,** I ask the client's legal contact or a lawyer before testing, not after.

## 9. Pre-engagement checklist

I copy this list for each engagement and do not start until every box is ticked.

- [ ] Written authorization signed by the system's legal owner
- [ ] Scope listed: IPs, domains, applications, cloud accounts, and what is excluded
- [ ] Testing window and time zone agreed
- [ ] Allowed and forbidden techniques written down (DoS, social engineering, physical)
- [ ] Emergency contact and stop procedure confirmed
- [ ] Cloud provider and third-party policies checked
- [ ] Data handling, storage and deletion terms agreed
- [ ] Tools verified and lab or attack box isolated
- [ ] Report format, recipients and deadline agreed
- [ ] I am competent for this work, or I have said where I am not

## 10. Violations, review and references

If I break this code, I own it: I stop, tell the affected owner, help fix any damage and write down what I will change.

- **If I see someone else break it,** I raise it with them first, then with the right authority (instructor, employer, certification body) if the harm is serious. ISC2 and EC-Council both run formal ethics complaint processes.
- **Review:** I reread and update this code once a year, when I earn a new certification, and when Guatemala's cybercrime law changes.
- **Precedence:** laws, contracts and employer policies win over this code where they are stricter; this code wins where they are silent.

**Codes this document draws on**

- [ISC2 Code of Ethics](https://www.isc2.org/ethics): four canons in order of precedence, binding for all ISC2 certifications
- [ISC2 Code of Professional Conduct](https://www.isc2.org/Insights/2026/03/code-of-professional-conduct-the-why-and-how): launched in 2026, builds on the canons and applies to certified and non-certified professionals
- [EC-Council Code of Ethics](https://www.eccouncil.org/code-of-ethics/): confidentiality, consent for personal data and intellectual property rules for CEH holders
- [Williams College CS331 Code of Ethics](https://williams-cs.github.io/cs331-f21-www/assets/handouts/03_code_of_ethics.pdf): an academic security course pledge with a signature line, adapted from EC-Council

## 11. Signature and attestation

I, the undersigned, have read this Personal Code of Conduct for Ethical Hacking and commit to follow it in my studies, my work, my independent projects and my teaching. I understand that holding offensive security skills is a privilege that depends on public trust, and that breaking this code can harm real people and expose me to academic, professional and legal consequences.

| Field | Entry |
| --- | --- |
| Full name | Roberto Hernandez |
| Signature | Roberto Hernandez |
| Date | 11 / 22 / 2026 |
| Place | Guatemala, Guatemala |
| GitHub | RoberttHernan |

**Annual review log**

| Review date | Changes made | Initials |
| --- | --- | --- |
| 11/22/2026 | none | R. H |
|  |  |  |
|  |  |  |
