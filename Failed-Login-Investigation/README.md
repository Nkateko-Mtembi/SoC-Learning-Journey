<img width="1366" height="768" alt="Screenshot 2026-06-17 002516" src="https://github.com/user-attachments/assets/a7529a12-0bf7-40bd-8f73-4d8d3174a0a9" />
<img width="1366" height="768" alt="Screenshot 2026-06-17 002509" src="https://github.com/user-attachments/assets/ca32de22-2a64-4cc6-96ef-292503969c4f" />
<img width="1366" height="768" alt="Screenshot 2026-06-17 002458" src="https://github.com/user-attachments/assets/6cccdbaa-fd25-4346-825b-b1b4ea0a256d" />

# Event ID 4625 - Failed Logon Investigation

# Objective 
Investigate a Windows Event and determine whether this was a failed logon attempt or a false positive.

# Alert Details
- Event ID: 4625
- IP: 192.168.0.231
- Target Account: Fakeuser
- Failure Reason: Unknown username or password

  # Investigation

  Multiple failed authentication attempts were detected from IP 192.168.0.231 targeting account fakeuser.
  A total of 10 failed logon attempts occurred within the timeframe of 35 seconds.
  No successful logon attempt was observed from this IP.

  An analysis of security event ID 4625 indicates failed logon attempts with status 0xc000006d and subStatus 0xc0000064,
  which signifies that the specified user account does not exist.

  The attempts originate from localhost::1, this suggests that the authentication requests were locally generated
  rather than from a remote external source.

  Futher investigation is recommended to determine whether these events were caused by user error, misconfigured software, scheduled tasks
  or unauthorized account enumeration activity.
