# REQ-PROFILE: Adivsor questionnaire

As an advisor, I want the agent to ask my client 10 questions before
any research, so that suggestions match the client's situation.

Acceptance criteria:
AC-1 The agent asks all 10 questions before any research starts
AC-2 An invalid answer is rejected and the question is asked again
AC-3 Answers are saved to a profile file with today's date
AC-4 If the profile is incomplete, research does not start
AC-5 The profile gets a risk band: Cautious, Balanced or Aggressive
