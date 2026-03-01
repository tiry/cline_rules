
## Task Flow

When collaborating on a project, work will be organized into **tasks**.

Each task starts from a user-defined input prompt.
From this prompt:

1. **Ask clarifying questions** if needed.
2. **Propose an implementation plan**.
3. Once the user validates the plan:

   * Create a **specification document** in the `specs/` folder.

     * Name the file: `<step_number>-<short_description>.md`
     * The spec should outline the plan clearly but concisely (avoid too much code).

During the task:

* Keep the **spec file**, **README**, and **unit tests** updated as work progresses.
* The task ends when the user explicitly tells you to commit.

At each iteration you should propose to:

 * run the build
 * execute unit tests

At task completion:

* Ensure all modified files are staged for commit.
* Propose a **concise, informative commit message** summarizing the work done.
* Let the user handle the actual `git push`.


## Tidy up code

When we rich the end of task implementation we need to check that we leave the code in a clean slate:

 - remove any dead code or files
 - check for duplicated code that could be shared

## Definition of Done (DoD)

A task is NOT complete until the following "Verification Loop" is green:

1. **Linting:** Run `ruff check` on modified files.
2. **Testing:** Run the specific test file associated with the change (e.g., `pytest tests/test_logic.py`).
3. **Regressions:** If the change affects core logic, run the full suite.
4. **Persistence:** If a test fails, you must attempt **at least 3 distinct hypotheses** before reporting an impasse.
5. **No False Flags:** Never state "The task is done" if tests are failing. If you cannot fix a test, clearly state: "STALLED: [Reason] [Stack Trace]."

If some tests are broken, we need to fix them before completing the task even is the work on this task is not the root cause of the tests failling.
