Modernization from COBOL to Java of folder: 978-1-4302-6253-4_Coughlan_Ch02

In general:
- when in doubt, ask the user for more information, don't assume, especially when it comes to business logic

Step 1: Reverse Engineering
- Understand what the legacy COBOL code actually does
- Identify input/output operations 
- Identify dependencies
- create a mermaid diagram to visualize the flow of the program
- document the business logic in a extra markdown file named `business-logic.md`

Step 2: Prepare the COBOL code
- Generate structured comments or markdown tables outlining:
    - Data type mappings.
	    - Equivalent control flow.
	    - Replacement of I/O and DB operations.
- Propose microservices decomposition if applicable.

Step 3: Prepare the translation to Java
- Identify Java libraries or frameworks that can be used to replace COBOL functionality. Write the libraries down in a `libraries.md` file.
- Create a mapping of COBOL constructs to Java constructs. Write them down in a `mapping.md` file.
- Write tests based the business logic written in the `business-logic.md` file.
- ensure 100% test coverage

Step 4: Translate the COBOL code to Java
- use the tests and the `libraries.md` and `mapping.md` files to translate the code