Analyze the following context in an attempt to find the bug(s):

- Provided context:
  - The context can be anything that I as a Senior Software Engineer think is applicable to helping you identify the issue.
  - This list of possible context items is not intended to be exhaustive, but the context could possibly include:
    - A description of the bug
    - My suspicions of what could be the root cause
    - Applicable files and/or code snippets related to the execution flow the bug is occurring in
    - A git diff showing changes made which introduced the bug
      - If the Git diff has logging, then I'm likely trying to convey to you useful context
        - Comments which start with "Failed" identify the specific tests which are failing
        - Comments which start with "Debug" identify:
          - The execution flow the error is occurring in
          - The specific method or function the error is occurring in
          - Things I thought seem suspicious
          - Theories regarding the source of the error I'd like you to consider
    - Pipeline (or terminal) logs which contain logs, errors, and stack traces
    - Lint errors
    - Compile errors
    - Configuration files
    - Dependencies used and their versions
    - File & folder structures
- Exploration:
  - List the several of the top-most likely possible root causes (e.g. type mismatches, async race conditions, logic errors, configuration issues, syntax issues, etc).
  - Present each cause as a succinct one-sentence bullet point.
- Prioritization:
  - Identify the top one or two most likely root cause(s).
  - Briefly explain why these are the strongest candidates.
- Validation & Next Steps:
  - Propose specific logging statements or assertions (include minimal code snippets) to verify your assumptions or provide additional context.
  - Propose additional context which would be useful that you're missing.
  - Recommend the next action choosing from one of the following options: “Insert these logs to confirm my suspicion…” or “Implement this bug fix...” depending on how confident you are that you've identified the issue.
  - Only suggest and outline how to implement a bug fix if you have high confidence that you've already identified the bug.

Input:
