# Template Angular app with Bazel & ngrx



## Installation

Install Bazel from the distribution, see [install] instructions.
On Mac, just `brew install bazel`.

Bazel will install a hermetic version of Node, npm, and Yarn when
you run the first build.

[install]: https://bazel.build/versions/master/docs/install.html

Also add `ibazel` to your `$PATH`:

```
yarn global add @bazel/ibazel
```

or

```
npm install -g @bazel/ibazel
```

## Setup

Before building the app, we install packages, just as with any npm-based development workflow.
However, to get the same version of the toolchain as co-workers and our continuous integration, let's have Bazel run the
package manager using a pinned version it manages. You should not even need
node, npm, or yarn installed on a machine where you develop with Bazel.

```bash
$ bazel run :install
```

## Development

Next we'll run the development server:

```bash
$ ibazel run src:devserver
```
