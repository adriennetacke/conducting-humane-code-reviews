# Conducting Humane Code Reviews

## Intro 
- Who has performed a code review?
- Who likes doing a code review?

## Combined w/ personal experience, here are top complaints:

## Code Review Pet Peeves
- #1 Subjective vs Objective
- Tone of voice in comments
- Loopholes in the process

## Why do humans do code reviews? (The last piece of the process that is not automated!)

## Ideal Code Review Goals
- Catch design flaws
  - Does the code make sense?
  - Is this the right codebase?
  - Does it integrate with the rest of your codebase nicely?
- Ensure code is coherent and clear
  - Can I understand it?
  - Is it too complex?
    - Complexity = harder to refactor, greater chance for bugs
- Validate code is needed (requested change/fix) or improves overall codebase
  - Does this improve the overall health of your codebase?
  - Is this needed at this time?
- Confirm functionality
  - Especially in UI changes
  - Does it do what it's supposed to?

## Let's break down those pet peeves one-by-one and see how we can combat it

## Subjective vs Objective

### What's subjective?
- Styling
- Naming
- Formatting
- Premature optimization suggestions (when none are important for this change)

*Examples

### What's objective?
- Overall design
  - Correct codebase vs library
  - Integrates with rest of codebase
- Timing
  - Is this dependent on other changes?
  - Waiting on fix for related system?
- Does it do what developer intended?
  - User-facing changes especially need to be validated
- Missed race-conditions/deadlocks
- Complexity
  - Too hard to understand
  - Over-engineered
- Premature optimizations (opposite, EXTRA functionality that is not needed for this change)

*Examples

### What to do instead!
- Automate what you can! 👉🏼 Takes care of styling, formatting nitpicks
  - Linters are your friend
  - Run all the tests!
  - Style Guide developed together 👉🏼 Takes care of naming, styling

## Tone of Voice in Comments

### **TL:DR** DON'T BE A JERK!

*Examples

## Slow Response Rate

- Reviewers are devs too
- PRs that are HUGE
  - Spoiler: Less likely to respond because there's so much to sift through

### What to do instead!
- Split PRs into manageable chunks
  - For PRs that can't be broken down:
    - Leave broader comments about overall design
    - Unblock dev as quickly as possible
    - Demand code review (DebtTrader)
- Never compromise own work to do code review
  - Get to a save point, then go on
  - Suggest other devs who have free cycles

## Loopholes in the Process

### What loopholes?
- Bias
  - Asking same people to review
  - Teaming up to approve each other's code
  - Only one approval required
  - Assuming "rockstar" dev's code is perfect 
- Bypassing review altogether
  - No protective policies in place for branches
  - Managers/Superadmins/Whoever skips normal review process
- MVE - Minimum Viable Effort
  - Skimming through
  - "Looks good to me!" 5 seconds after PR is opened
  - Lack of honest effort

### What to do instead!
- Auto-add ALL devs to all PRs 👉🏼 Tackles bias, MVE
  - Code Owners in GitHub - Auto adds topic-specific devs if certain files are changed (those closer to codebase)
  - https://help.github.com/en/articles/about-code-owners
- Require 2 or more approvals (the more the better!) 👉🏼 Tackles bias, Bypassing review, MVE
- Add policies! 👉🏼 Tackles bias, Bypassing review
  - No force push abilities to master
  - No force push abilities for anyone!
- Regardless of WHO wrote code, all code changes go through same process 👉🏼 Tackles bias, Bypassing review


### Things humans should do
- *Suggest* with facts
- *Reject* with courtesy
- *Respond* in a timely manner and only when you are at a break point
- *Clarify* with an open-mind





--------------------------------------------
Unordered


### Things robots should do
- Enforce style guide
  - Trailing commas vs non-trailing commas
  - Spacing
  - Naming conventions
  - Syntax errors (missing semicolons)


