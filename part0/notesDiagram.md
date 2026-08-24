```mermaid
graph TD;
    A[user inputs text into text field] --> B[user clicks save to submit form, sends server POST request] --> C[Server receives request, checks headers and payload]

    C -- Success --> Accepts new note and posts/adds content to the list of notes
    C -- Error --> Does not accept new note and returns an error with description on the error or issue

    D[Page is refreshed with new GET request of notes]
```