Instead of serving business logic directly by a request we would convert that request into command and then pass that command to business logic and then the command will give result back to request.

- Parameterize objects with different requests.
- Queue or log requests.
- Support undoable operations.