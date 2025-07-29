
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
