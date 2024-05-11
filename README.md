![Create Release Workflow](https://github.com/tscharke/useIntersection/actions/workflows/createRelease.yml/badge.svg?push=tags) ![Release](https://img.shields.io/github/v/release/tscharke/useIntersection?display_name=release&label=Release)

# useIntersection hook

This project is a custom hook for React that uses the IntersectionObserver API to observe a DOM element.

## When to use `useIntersection` and `useIntersectionRef`?

### `useIntersection`

classical useIntersection hook with useEffect and useRef

### `useIntersectingRef`

same as `useIntersection` but with avoiding the need to use useEffect and useRef, allows intersection on optional or delayed elements

## Getting Started

### Prerequisites

- Node.js
- pnpm

### Installing

```bash
pnpm i
```

### Running the tests

```bash
pnpm test
```

### Building

```bash
pnpm build
```

## Create a new release

To create a new release, it is necessary to **set** and **push** a (Git)Tag like:

```bash
git tag v1.2.3 && git push origin v1.2.3
```

What is crucial here is that the tag begins with a lowercase `v` followed by a [Semantic Versioning](https://semver.org/) -
a tag will then look like this: `v1.2.3`.

From this, a [GitHub Action](https://docs.github.com/en/actions) then creates a tar file with the name by this pattern:

```
${NAME_OF_THIS_PROJECT}-${SEMANTIC_VERSIONING_OF_TAG}.tar.gz

// Output: useintersection-1.2.3.tar.gz
```

Which tar file can be used as a dependency in other projects. To do this, this tar file must be downloaded and can then be
used installed in another project like this:

```bash
pnpm install ../../my-location/useintersection-1.2.3.tar.gz
```

## Built With

- [React](https://reactjs.org/) - The web framework used
- [TypeScript](https://www.typescriptlang.org/) - The language used
