# 1. Document Analysis & Requirements Gathering

## Inventory all current runtime keys and their associated metadata

- **edge-routine**
	- Organization: Alibaba Cloud
	- Website: [https://www.alibabacloud.com/help/en/dynamic-route-for-cdn/latest/er-overview](https://www.alibabacloud.com/help/en/dynamic-route-for-cdn/latest/er-overview)
	- Description: The JavaScript/WebAssembly runtime that powers Alibaba Cloud edge-routine.

- **arvancloud**
	- Organization: Arvancloud
	- Website: [https://www.arvancloud.ir/en/products/edge-computing](https://www.arvancloud.ir/en/products/edge-computing)
	- Description: The JavaScript runtime that powers Arvancloud Edge Computing.

- **azion**
	- Organization: Azion
	- Website: [https://www.azion.com/en/products/edge-functions/](https://www.azion.com/en/products/edge-functions/)
	- Description: Azion Edge Functions for ultra-low latency, edge-native applications, built with open standards for secure, high-performance serverless computing.

- **workerd**
	- Organization: Cloudflare
	- Website: [https://workers.cloudflare.com/](https://workers.cloudflare.com/)
	- Description: The JavaScript / WebAssembly runtime that powers Cloudflare Workers.
	- Repository: [https://github.com/cloudflare/workerd](https://github.com/cloudflare/workerd)

- **deno**
	- Organization: Deno Land
	- Website: [https://deno.com](https://deno.com)
	- Description: A modern runtime for JavaScript and TypeScript.
	- Repository: [https://github.com/denoland/deno](https://github.com/denoland/deno)

- **lagon**
	- Organization: Lagon
	- Website: [https://lagon.app](https://lagon.app)
	- Description: Open-source runtime and platform for running TypeScript and JavaScript Functions at the Edge.
	- Repository: [https://github.com/lagonapp/lagon](https://github.com/lagonapp/lagon)

- **react-native**
	- Organization: Meta
	- Website: [https://reactnative.dev/](https://reactnative.dev/)
	- Description: A framework for building native apps using React. Represents supported React Native JS runtimes on native platforms (excludes react-native-web).
	- Repository: [https://github.com/facebook/react-native](https://github.com/facebook/react-native)

- **moddable**
	- Organization: Moddable
	- Website: [https://www.moddable.com/](https://www.moddable.com/)
	- Description: Open source runtime for resource-constrained embedded devices using standard JavaScript and TypeScript. Supports standard ECMA-419 APIs.
	- Repository: [https://github.com/Moddable-OpenSource/moddable](https://github.com/Moddable-OpenSource/moddable)

- **netlify**
	- Organization: Netlify
	- Website: [https://docs.netlify.com/edge-functions/overview/](https://docs.netlify.com/edge-functions/overview/)
	- Description: Edge Functions connect the Netlify platform and workflow with an open runtime standard at the network edge.
	- Repository: [https://github.com/netlify/edge-functions](https://github.com/netlify/edge-functions)

- **electron**
	- Organization: OpenJS Foundation
	- Website: [https://www.electronjs.org/](https://www.electronjs.org/)
	- Description: Build cross-platform desktop apps with JavaScript, HTML, and CSS.
	- Repository: [https://github.com/electron/electron](https://github.com/electron/electron)

- **node**
	- Organization: OpenJS Foundation
	- Website: [https://nodejs.org](https://nodejs.org)
	- Description: Node.js is an open-source, cross-platform JavaScript runtime environment.
	- Repository: [https://github.com/nodejs/node](https://github.com/nodejs/node)

- **bun**
	- Organization: Oven
	- Website: [https://bun.sh/](https://bun.sh/)
	- Description: Incredibly fast JavaScript runtime, bundler, transpiler and package manager - all in one.
	- Repository: [https://github.com/oven-sh/bun](https://github.com/oven-sh/bun)

- **react-server**
	- Organization: React
	- Website: [https://react.dev/](https://react.dev/)
	- Description: Used by React Server Components.
	- Repository: [https://github.com/facebook/react](https://github.com/facebook/react)

- **edge-light**
	- Organization: Vercel
	- Website: [https://edge-runtime.vercel.app/](https://edge-runtime.vercel.app/)
	- Description: Developing, testing, and defining the runtime Web APIs for Edge infrastructure.
	- Repository: [https://github.com/vercel/edge-runtime](https://github.com/vercel/edge-runtime)

- **fastly**
	- Organization: Fastly
	- Website: [https://developer.fastly.com/learning/compute/javascript/](https://developer.fastly.com/learning/compute/javascript/)
	- Description: JavaScript runtime for Fastly Compute@Edge.
	- Repository: [https://github.com/fastly/js-compute-runtime](https://github.com/fastly/js-compute-runtime)

- **kiesel**
	- Organization: Kiesel
	- Website: [https://kiesel.dev/](https://kiesel.dev/)
	- Description: A JavaScript engine and runtime written in Zig.
	- Repository: [https://codeberg.org/kiesel-js/runtime](https://codeberg.org/kiesel-js/runtime)

- **wasmer**
	- Organization: Wasmer
	- Website: [https://wasmer.io/products/edge](https://wasmer.io/products/edge)
	- Description: The JavaScript runtime that brings JavaScript to Wasmer Edge.
	- Repository: [https://github.com/wasmerio/winterjs](https://github.com/wasmerio/winterjs)

## Document the current change control process and approval mechanisms

The current process is best summarized as opening a PR to the GitHub repo https://github.com/WinterTC55/runtime-keys adding or modifying the list of keys within the unofficial draft specification we initially created. An entry must follow the format of the existing entries, and is manually reviewed by the WinterTC55 (prev. WinterCG) group members. Once approved, the entry is merged and the document is updated. 

Ignoring the specific formatting rules and contribution process, the general change control process is

- All JavaScript runtimes are welcome to create a key and add it to the list.
- New keys must not conflict with another existing key.
- Runtime entries on this list are encouraged, but not required, to participate in the community group.
- Keys should meaningfully represent the relevant runtime and be a simple, string-like value so it can be used in common configuration formats such as JSON and YAML.
- Keys should also not conflict with existing [Browserlist entries](https://github.com/browserslist/browserslist#browsers).
- Keys are subject to the discretion of the WinterTC55 group members review. Keys should:
  - Avoid being too similar to existing keys.
  - Avoid similarity to common english words or offensive terms.
  - Avoid being too generic or similar to the general terminology of "Web Runtimes", "Edge Runtimes", "JavaScript Runtimes", etc.
- Modifying keys is not allowed, as it would break existing configurations that use the key.
  - But modification of a key's metadata is allowed, such as updating the description or adding a new website.
- Keys can be deprecated to indicate inactive organization/projects.
- Deprecated keys can be undeprecated as long as it is the original organization/project resumes activity.
- Implementations should not add support for a deprecated key.

## Identify stakeholders

The key stakeholders is mainly OpenJS Foundation Package Metadata Interoperability Working Group and the WinterTC55 group. It is expected that maintainers of any implementations or tooling around this registry are participating in one or both of these groups.

> The members of these groups are the ones who are doing the main work on this

Additionally, we need to involve all existing runtimes in the existing list one way or another.

Must at least attempt to reach out, but can accept no-reply as an exclusion from the initial IANA registry list??

