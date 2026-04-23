## Project Structure

There is NextJS project in the `/next`.


## Next

Rules in this section and its subsections applied only to the NextJS project in the `/next` dir.

<!-- BEGIN:nextjs-agent-rules -->
This is NOT the Next.js you know.

This version has breaking changes — APIs, conventions, and file structure may all differ from your training data. Read the relevant guide in `next/node_modules/next/dist/docs/` before writing any code. Heed deprecation notices.
<!-- END:nextjs-agent-rules -->

### Bun

This project uses bun instead of npm or other package managers. Command `bun dev` is always running in the background, you SHOULD NOT try to run this command. You SHOULD NOT try to build project with `bun run build` to check your work.

### Format, Linting, Typecheck

You SHOULD run `bun fix` in the end of your task. You SHOULD check the output of the command and fix errors manually if there are any. After that you SHOULD run `bun check`. You SHOULD check the output of the command and fix errors manually if there are any.

### Testing

You SHOULD only use default bun test runner as testing framework. You SHOULD NOT use vitest or other frameworks.

You SHOULD prefer Integration/Functional tests over granular unit tests for features. You SHOULD mock only hardware like databases or external APIs. You SHOULD NOT mock server actions, hooks, or component logic when testing features.

Use descriptive names reflecting use cases. Prefix names with emojis to differentiate test types:
    🧪 Integration / Functional tests
    ⚡ Unit tests

You SHOULD run `bun test` in the end of your task after format, linting and typecheck. You SHOULD check the output of the command and fix tests manually if there are any.

### UI Components

For UI components you SHOULD use shadcn ui. You SHOULD install component with command `bunx --bun shadcn@latest add` instead of manual creation of it. You SHOULD use shadcn Base UI instead of Radix UI.