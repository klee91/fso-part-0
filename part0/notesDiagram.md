```mermaid
graph TD;
    A[user inputs text into text field] --> B[user clicks save to submit webform, sends server POST request (
https://studies.cs.helsinki.fi/exampleapp/new_note)] --> C[Server receives request, checks headers and payload]

    C -- Success --> D[Accepts new note and posts content to the list of notes]
    C -- Error --> E[Does not accept new note and returns an error with description on the error or issue]

    D ----> F[Page displays notes with new AJAX GET request of notes (https://studies.cs.helsinki.fi/exampleapp/data.json)]
    E ----> F[Page displays notes with new AJAX GET request of notes (https://studies.cs.helsinki.fi/exampleapp/data.json)]
```