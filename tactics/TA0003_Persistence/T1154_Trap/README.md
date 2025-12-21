# T1154 – Trap

## Tactic
TA0003 – Persistence

## Description
The <code>trap</code> command allows programs and shells to specify commands that will be executed upon receiving interrupt signals. A common situation is a script allowing for graceful termination and handling of common  keyboard interrupts like <code>ctrl+c</code> and <code>ctrl+d</code>. Adversaries can use this to register code to be executed when the shell encounters specific interrupts either to gain execution or as a persistence mechanism. Trap commands are of the following format <code>trap 'command list' signals</code> where "command list" will be executed when "signals" are received.(Citation: Trap Manual)(Citation: Cyberciti Trap Statements)

## Data Sources
N/A

## Detection Ideas
- TODO

## False Positives
- TODO

## Response Actions
- TODO

## References
- https://attack.mitre.org/techniques/T1154/
