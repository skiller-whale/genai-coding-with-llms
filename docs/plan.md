Rules:
    - Create an app that parses markdown files of the following format:
    
    ```md
    # Ticket Name

    ## Description
    A ticket created by the customer support team in plaintext.

    ## Tasks
    - A bullet point.
    - A second bullet points.
    - Only bullet points and nothing else allowed under `##Tasks`.
    ```

    - Give me sample files as well. Those should convert to JSON. For example, the above should convert to:
    
    ```json
    {
        'name': 'Ticket Name',
        'description': 'A ticket created by the customer support team in plaintext.',
        'tasks': [
            'A bullet point.'
            'A second bullet point',
            'Only bullet points and nothing else allowed under `##Tasks`.'
        ]
    }
    ```

    - Include a set of tests using `jsonschema` that validate the above format.
    - Nothing else is allowed in the markdown files.
    - Use `markdown_it` in Python to process and validate the markdown files.

