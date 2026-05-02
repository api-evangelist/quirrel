# Quirrel

Quirrel (https://quirrel.dev) is an open source job queueing and workflow scheduling service designed for serverless and containerized JavaScript and TypeScript applications. It gives developers a simple way to enqueue, delay, schedule, retry, and orchestrate background jobs without managing dedicated worker infrastructure. Quirrel was acquired by Netlify in 2022 and remains available as an open source project.

## Quirrel Queue API

The Quirrel SDK exposes a Queue API for managing background jobs. Common methods include:

- `enqueue(payload, options)` - Schedule a single job with optional `id`, `runAt`, `delay`, `repeat` (cron / interval), `retry`, and `exclusive` flags.
- `enqueueMany(jobs)` - Enqueue up to 1000 jobs in a single call.
- `get()` - Generator function that iterates over pending jobs.
- `getById(id)` - Retrieve a specific job by ID.
- `invoke(id)` - Execute a pending job immediately.
- `delete(id)` - Remove a pending job from the queue.

Quirrel supports cron-based recurring jobs, delayed execution (for example `delay: "7d"`), exclusive jobs that serialize execution, and configurable retry intervals (up to 10 attempts).

### Framework Support

Quirrel integrates with most popular JavaScript frameworks and serverless platforms, including:

- Next.js
- Blitz.js
- RedwoodJS
- Remix
- SvelteKit
- Nuxt.js
- Express / Connect
- Vercel Functions
- Netlify Functions

### API Resources

- **Documentation:** https://docs.quirrel.dev
- **Getting Started:** https://docs.quirrel.dev/getting-started
- **Source Code:** https://github.com/quirrel-dev/quirrel
- **npm Package:** https://www.npmjs.com/package/quirrel

## OpenAPI Specification

Quirrel is consumed primarily through its TypeScript / JavaScript SDK, and there is no public REST OpenAPI specification published in this repository.

## Links

- **Website:** https://quirrel.dev
- **Documentation:** https://docs.quirrel.dev
- **Source Code:** https://github.com/quirrel-dev/quirrel
- **Acquisition Announcement:** https://www.netlify.com/blog/quirrel-is-joining-netlify/

## Maintainers

- **FN:** Kin Lane
- **Email:** kin@apievangelist.com
