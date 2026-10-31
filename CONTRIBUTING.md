# Contributing

This project is run like a team project: every change lands on `main` through a reviewed pull request.

## Workflow

1. **Start from an issue.** Each slice of work has an issue on the [project board](https://github.com/users/h4wl/projects/2). Move it to **In Progress** when you start.
2. **Branch from `main`** using a prefix that describes the change:
   - `feat/…` new functionality
   - `fix/…` bug fixes
   - `chore/…` tooling, CI, dependencies, docs
3. **Keep PRs to one slice.** A PR should be small enough to review in one sitting. Split larger issues into several PRs.
4. **Open a pull request** into `main`. Link the issue with `Closes #<number>` in the description so merging closes it and moves its card to **Done**.
5. **Review before merging.** Every PR gets a full code review. Review comments are posted on the PR, and all conversations must be resolved before it can merge.
6. **Squash merge.** The PR title becomes the commit on `main`, so write it as a clear summary of the change. The branch is deleted automatically after merge.

## Branch protection

`main` is protected by the **Protect main** ruleset, which applies to everyone, including the repo owner:

- Changes require a pull request (no direct pushes)
- All review conversations must be resolved
- CI must pass
- Squash merge only, with linear history
- No force pushes or deletion

## Checks

CI runs on every pull request and on pushes to `main`. Run the same checks locally before pushing:

```sh
npm run typecheck
npm test
```

## Local development

Requires Node 24.3 or later.

```sh
npm i
npm run dev
```

The app runs at http://localhost:44100.
