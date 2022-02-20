# graphql-eslint-error

I have opened the following issue: https://github.com/B2o5T/graphql-eslint/issues/947

There is a open issue in Stack Overflow that explains the error: https://stackoverflow.com/questions/70943271/graphql-eslint-eslint-plugin-parseroptions-schema-error

Steps to reprduce:
1. clone repository
2. build and install the project (I was using yarn)
3. Try to run eslint

You will came across the following error: "ESLint: Rule 'unique-argument-names' requires 'parserOptions.schema' to be set and schema to be loaded. See http://bit.ly/graphql-eslint-schema for more info Occurred while linting /Users/royleibovitz/IdeaProjects/myProject/my-project/src/graphql/application/application.schema.graphql:0 Rule: "@graphql-eslint/unique-argument-names". Please see the 'ESLint' output channel for details."

The error is caused by the following rule: "@graphql-eslint/unique-input-field-names"
The same error appears for all rules that required to lint the whole schemas and operation files.

I have tried too many values for the parserOptions.schema field, but any of them solved it.
