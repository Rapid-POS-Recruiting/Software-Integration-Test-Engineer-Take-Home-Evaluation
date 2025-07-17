# Software-Integration-Test-Engineer-Take-Home-Evaluation
This document will list the steps a candidate for the Software Integration & Test Engineer I position will perform to evaluate skill level, proficiency, and ability to deliver a solution meeting the requirements in a timely manner.
## Requirements
- IDE or Text Editor: Such as Visual Studio Code, PyCharm, or any preferred code editor.
- Database engine: SQL Server, PostgreSQL, SQLite, etc.
- Programming Language: Python, Java, C#, or any language you are comfortable with.
- Testing Framework: JUnit, NUnit, PyTest, or any preferred testing framework.
- Version Control: Git, GitHub, or any preferred version control system.
- CI/CD Tool: Azure DevOps, Jenkins, GitHub Actions, or any preferred CI/CD tool.
- Mocking Tool: Postman, WireMock, or any preferred mocking tool.
- Optional: Android development environment if you choose to complete the bonus task.
## Overview
You will be creating a test plan, developing automation scripts, and setting up a CI pipeline to
test a mock payment gateway API. The API simulates a checkout process where a user can pay for items using different credit cards. The goal is to ensure the API behaves correctly under various scenarios, including successful and declined payments.
## Instructions
1. **Clone the Repository**: Start by cloning the provided repository containing the mock API and
    the sample database schema. The repository URL will be provided in the job posting.
2. **Set Up the Environment**: Ensure you have the necessary tools and dependencies installed to run the mock API and database. This may include Docker for running the PostgreSQL instance and any other dependencies required by the mock API.
3. **Understand the API**: Familiarize yourself with the mock API endpoints, particularly the `POST /checkout` endpoint. This endpoint simulates a checkout process where a user can pay for items using different credit cards.
4. **Database Schema**: Review the provided database schema, which includes tables like `sales_hdr` and `sales_lin`. Understand how these tables are used to store sales transactions and payment statuses.
5. **Test Cases**: Identify the key test cases that need to be automated. This includes scenarios for successful payments, declined payments, and verifying the database state after transactions.
6. **Automation Scripts**: Write automation scripts to test the `POST /checkout` endpoint. The scripts should cover the following scenarios:
    - A successful payment with a valid credit card.
    - A declined payment with an invalid credit card.
    - Verifying the database state after each transaction.
7. **CI Pipeline**: Set up a CI pipeline to automate the testing process. The pipeline should:
    - Restore and build the code.
    - Spin up a PostgreSQL instance using Docker.
    - Run the automation scripts and publish JUnit/coverage reports.
    - Ensure that the pipeline fails if the code coverage is below 70%.
8. **Documentation**: Document your test plan, automation scripts, and CI pipeline setup in a README file. Include instructions on how to run the tests and any additional information that may be helpful for someone reviewing your work.
9. **Bonus Task (Optional)**: If you are comfortable with Android development, write an Espresso or Robolectric test for the included Checkout app that scans two barcodes, taps Pay, and verifies the success toast.
10. **Submission**: Once you have completed the tasks, push your code to a GitHub repository. Ensure that the repository is well-organized and includes a README file with your full name and the method or job site you used to reach this repository. Send an invitation to your GitHub repository to Rapid POS at `recruiting.programmer@rapidpos.com`.
