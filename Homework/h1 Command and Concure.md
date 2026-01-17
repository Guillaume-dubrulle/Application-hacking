# a) Baseline

## 1. What is included in scope

- the router
- my laptop
- my phone 

## 2. What you exclude and why
- ISP’s network (don't own it)

## 3. Key interfaces

- moodle
- github


| in scope            |                | out of scope    |
| ------------------- | -------------- | --------------- |
| my laptop -> router | -> firewall -> | github / moodle |



# b) Tie It to the Standard



| Interested party                 | Need / expectation / requirement                      | ISO 27001 requirement area                             | evidence                                                              |
| -------------------------------- | ----------------------------------------------------- | ------------------------------------------------------ | --------------------------------------------------------------------- |
| Me, owner of my network, student | Availability of the laptop and network for the course | Context (4), Leadership (5), Operation (8)             | acceptance of risks documented                                        |
| Educational institution          | Academic integrity                                    | Context (4), Operation (8), Performance evaluation (9) | strong passwords and MFA on Moodle/GitHub                             |
| Cloud services                   | Account security, compliance with terms of service    | Operation (8), Improvement (10)                        | MFA enabled, password manager usage, access via personal devices only |
| Internet service provider (ISP)  | no abusive or illegal activity                        | Context (4), Leadership (5)                            | router firewall enabled, no open ports unless justified               |
