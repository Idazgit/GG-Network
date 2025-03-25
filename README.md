# GG Network

Welcome to **GG NETWORK**, a platform dedicated to gamers and content creators! This project aims to bring together the community of players within groups, while allowing youtubers to initiate 100% safe contests and promote their content.

## Features

- Create and manage gamer groups
- Organize and participate in secure contests
- Customizable user profiles
- Discussion and sharing system between members

## Installation

### Prerequisites

- Node.js (v16 or higher)
- npm or yarn

### Project Installation

Clone the project repository:

```bash
git clone https://github.com/Idazgit/GG-Network.git
cd gg-network
```

Install dependencies:

```bash
npm install
# or
yarn install
```

## Development Tools Configuration

We use several tools to improve code quality and commit management.

### Linting and Formatting

- **ESLint**: Static code analysis to detect errors and inconsistencies.
- **Prettier**: Automatic code formatting for optimal consistency.

Configuration:

```bash
npm install --save-dev eslint prettier
```

### Commit Management

- **Husky**: Runs Git hooks to check the code before each commit.
- **lint-staged**: Applies ESLint and Prettier only to modified files.
- **commitlint**: Ensures commit messages follow a predefined format.
- **commitizen**: Simplifies writing commit messages in a standardized format.

Installation:

```bash
npm install --save-dev husky lint-staged commitlint commitizen
```

Add the following configurations in `package.json`:

```json
"husky": {
  "hooks": {
    "pre-commit": "lint-staged",
    "commit-msg": "commitlint --edit"
  }
},
"lint-staged": {
  "*.{js,jsx,ts,tsx}": "eslint --fix && prettier --write"
},
"commitlint": {
  "extends": ["@commitlint/config-conventional"]
}
```

Initialize Husky:

```bash
npx husky install
```

## Start the Project

Run the development server:

```bash
npm run dev
# or
yarn dev
```

## Contribute

1. Fork the project
2. Create a branch (`git checkout -b feature-new-feature`)
3. Commit your changes (`git commit -m "feat: add a new feature"`)
4. Push your branch (`git push origin feature-new-feature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.
