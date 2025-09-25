# Contributing to RetypeOS

First off, thank you for considering contributing to RetypeOS! 🎉 We are thrilled you're here. This project thrives on community contributions, and every bit of help is greatly appreciated. Whether it's reporting a bug, proposing a new feature, improving documentation, or writing code, you are helping us build the future of developer tooling.

This document is a guide to help you through the process.

## Code of Conduct

Before you start, please read our [Code of Conduct](./CODE_OF_CONDUCT.md). We are committed to fostering an open, welcoming, and inclusive environment, and we expect all contributors to adhere to these standards.

## How Can I Contribute?

There are many ways to contribute to the project. Here are a few ideas:

* **🐛 Reporting Bugs:** If you find a bug, please open an issue and use the "Bug Report" template. The more details you provide, the faster we can fix it.
* **💡 Proposing Enhancements:** Have an idea for a new feature or an improvement to an existing one? We'd love to hear it! Open an issue using the "Feature Request" template to start the discussion.
* **📖 Improving Documentation:** Great documentation is key. If you find something unclear, incorrect, or missing in our `README.md` or other docs, please submit a Pull Request with your improvements.
* **✍️ Writing Code:** If you're ready to get your hands dirty, you can pick up an existing issue (especially those tagged `good first issue` or `help wanted`) and submit a Pull Request.

## Your First Contribution

Unsure where to begin? A great way to start is by looking for issues tagged with:

* `good first issue`: These are issues that have been identified as good entry points for new contributors.
* `help wanted`: These are issues that we would particularly appreciate community help with.
* `documentation`: A fantastic way to learn the project's internals is by improving its documentation.

If you decide to take on an issue, please leave a comment to let us know. This helps us avoid duplicated work.

## Development Setup

To get `axes` (our flagship project) running locally, you'll need the latest stable version of Rust. You can install it via [rustup](https://rustup.rs/).

1. **Fork the repository:**
    Click the "Fork" button on the top right of the [axes repository page](https://github.com/RetypeOS/axes).

2. **Clone your fork:**

    ```sh
    git clone https://github.com/YOUR_USERNAME/axes.git
    cd axes
    ```

3. **Build the project:**
    A simple build will download all dependencies and compile the project.

    ```sh
    cargo build
    ```

4. **Run the tests:**
    We aim for high test coverage. Before you start making changes, make sure all tests are passing.

    ```sh
    cargo test
    ```
    <!-- Opcional: Si tienes tests de integración que requieren configuración, añádelo aquí. -->
    <!-- e.g., For integration tests, you might need Docker: `docker-compose up -d && cargo test -- --ignored` -->

5. **Run the application:**
    You can run your local build directly using `cargo run`. For example:

    ```sh
    cargo run -- --version
    cargo run -- . info
    ```

## Submitting a Pull Request

When you're ready to submit your changes, please follow these steps. This ensures a smooth and efficient review process.

1. **Create a new branch** for your feature or bugfix. Please use a descriptive name.

    ```sh
    # Example for a new feature:
    git checkout -b feature/add-parallel-execution

    # Example for a bugfix:
    git checkout -b fix/resolve-context-cache-bug
    ```

2. **Make your changes.**
    * **Code Style:** We follow the standard Rust conventions. Please run `cargo fmt` to format your code before committing.
    **Formatting:** We use `rustfmt` to maintain a consistent code style. Run it on your entire project: `cargo fmt --all`.
    * **Linter:** We use Clippy to catch common mistakes. Please run `cargo clippy -- -D warnings` and address any issues it reports.
    * **Commit Messages:** Please write clear and descriptive commit messages. We follow the [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/) specification. This helps us automate changelogs and understand the history of the project.
        * `feat:` A new feature.
        * `fix:` A bug fix.
        * `docs:` Documentation only changes.
        * `style:` Changes that do not affect the meaning of the code (white-space, formatting, etc).
        * `refactor:` A code change that neither fixes a bug nor adds a feature.
        * `test:` Adding missing tests or correcting existing tests.
        * `chore:` Changes to the build process or auxiliary tools.

3. **Add or update tests.**
    Your Pull Request should include tests that cover your changes. A new feature needs new tests, and a bug fix should ideally include a test that reproduces the bug to prevent regressions.

4. **Update documentation.**
    If your changes affect the user-facing behavior of the application, please update the `README.md` or other relevant documentation.

5. **Push your branch and open a Pull Request.**
    Push your changes to your fork and open a Pull Request against the `main` branch of the `RetypeOS/axes` repository.

6. **Fill out the Pull Request template.**
    The template is there to help you provide all the necessary information for the reviewers. Please fill it out as completely as possible.

7. **Wait for review.**
    A core maintainer will review your Pull Request. We may ask for changes or clarifications. We aim to be responsive and provide constructive feedback.

Thank you again for your interest in making RetypeOS better. We're excited to see your contributions!
