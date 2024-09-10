![](Aspose.Words.858be072-194b-4569-86df-c4fe6643b5ba.001.png)

**SUCURSAL APP**

*Developer’s Guide to Excellence*

**Project Structure**

- **App.tsx**: The core of our application where React is rendered.
- **Components**: All app components are stored here, each within its own .tsx file.
- **Screens**: Our Screens are (Login, Sign Up, Profile Questionnaire, Dashboard, Members, General Budget, Income/Expense Details, Settings, Profile)
- **Assets**: Resources used by the app are here, categorized by type:
- **jpg**: JPEG images.
- **svg**: Vector graphics such as icons.
- **png**:PNG images.
- **fonts**: Local fonts are stored in this folder.

**Utils** Utils: Contains modules and functions that are useful throughout the application. Files should be in TypeScript and adhere to the single responsibility principle. Names should be descriptive, use camelCase, and functions should be declared as constants with arrow function syntax.

Example:

- getTransactions: Retrieve transaction data from state or LocalStorage.
- listTransactionsByDate: List transactions in date order.
- calculateBalance: Calculate the overall balance from transactions.

**Services** Services: Contains modules and functions that interface with external services, such as APIs or libraries. Files should be in TypeScript, follow the single responsibility principle, and use descriptive names in camelCase. Functions should be constants declared with arrow functions.

Example:

- fetchTransactionsFromAPI: Retrieve transactions from an external API.
- postTransactionToAPI: Send a new transaction to the API.
- deleteTransaction: Delete a transaction from the API.

**Variables** Variables: Use camelCase for variable names, making them as descriptive as possible. Prefer const for constants, but use let for variables that need to change. Avoid using var completely.

Example:

- currentBalance: Current balance.
- categoryInput: Category input for the expense form.
- amountInput: Amount entered for the expense form.
- dateInput: Date entered for the expense form.
- **CSS and Fonts**: Each component has a dedicated CSS file. Responsiveness is managed using media queries:
- **Desktop Version**: Maximum width of 1700px, minimum of 1200px.
- **Mobile Version**: Maximum width of 480px, minimum of 320px.
- **Component Identification and Classes**: Use English for HTML element IDs and classes, following camelCase conventions. To avoid style conflicts, wrap each component in a container with a unique ID. Styles should refer to this ID.
- **Fonts**: Use locally downloaded fonts for typography. In assets/fonts, fonts.css contains all @font-face declarations, which are imported into components or the main HTML file.

**Component Structure**: To create a new component in your project, follow these steps:

1. **Add Component Folder**: Create a folder within components with the name of the component in PascalCase.
1. **Component Files**:
- Inside the component folder, include two files:
- A .tsx file with the same name as the component.
- A .css file with the same name as the component.
3. **Use Arrow Functions and PascalCase**: Components should be defined using arrow functions and should follow the PascalCase convention for the component name.
3. **Define Properties**: Define the component properties in an interface within the same .tsx file, named after the component with Props added.

**Example**:

For the component "AddExpenseForm":

- **Component Folder**: components/AddExpenseForm
- **File Structure**:
- components/AddExpenseForm/AddExpenseForm.tsx
- components/AddExpenseForm/AddExpenseForm.css

**Task**

1. **Jaime Vargas**

**Responsibilities:**

- Develop the backend structure in \*\*TypeScript\*\*, focusing on transaction and category management functionalities.
- Create the logic for adding, deleting, and modifying transactions within each category.
- Implement the database or temporary storage for finances.

  **Deliverables:**

- Initial project setup in \*\*Visual Studio\*\*.
- Logic for adding categories and transactions.
- Basic backend structure with data handling.
- Functional backend with integrated logic for adding and deleting funds.
- Simulation of transactions between different categories.
2. **Daniel Zapata**

**Responsibilities:**

- Design the user interface (UI) using \*\*React\*\*and \*\*CSS\*\*to make it intuitive and user-friendly.
- Create screens for:
  - Viewing categories.
  - Managing transactions.
  - Main screen displaying a general summary of finances.

**Deliverables:**

- Initial prototype of category and transaction screens.
- Design of reusable components in \*\*React\*\*.
- Fully functional user interface with smooth transitions.
- Optimization for mobile screens.
3. **Juan Tenorio**

**Responsibilities**:

- Integrate the logic developed by Jaime into the interface created by Daniel.
- Ensure that user interactions, such as adding or modifying transactions, are correctly reflected in the UI.
- Manage the application state using \*\*React Hooks\*\*or \*\*Redux\*\*to maintain synchronization between the frontend and the backend.

  **Deliverables:**

- Initial integration of transaction and category logic with the UI.
- State management for transactions and categories.
- Complete interaction between the interface and the backend.
- Functionality allowing dynamic addition, deletion, and modification of transactions from the UI.

**Git and Repository**

- Types of Commits:
  - fix:Bug fixes.
  - feat: New features.
  - build: Changes to the build system or dependencies.
  - docs: Documentation updates.
  - perf: Performance improvements.
  - refactor: Code changes that neither fix a bug nor add a feature.
  - style: Changes that do not affect code functionality (formatting, missing semicolons, etc.).
  - test: Adding or updating tests.
- Scopes:
  - hotfix: Minor fixes.
  - feature: Significant changes.
  - userStory: Very small changes.
- Description: Start commit titles with verbs like add, update, delete.

**Setup Instructions**

dev: Runs the application in development mode.

npm run dev

build: Builds the production-ready version of the app.

npm run build

preview: Starts a preview server for the built application before deployment. npm run preview

**Branching Model**

We use the branches main, develop, and feature. Merges are done through pull requests in VSCode. Ensure you’re on the correct branch before merging.

- **Main**: Contains the final, deployable version of the application.
- **Develop**: Used for major development changes, with features merging here.
- **Feature**: For small, specific changes, which can be integrated into other feature branches.
