# Processes
Processes are similar to [functions](Functions.md), but they have a few key differences. For starters, they are asynchronous, allowing you to create multiple threads in your program.
Processes additionally can be subscribed to [events](Events.md), allowing them to trigger whenever an event is triggered. You can subscribe a process to an event using the ``@`` character. Processes can be defined using the ``pro`` keyword.
```
pro ProcessName() @ PlayerJoinEvent { /* This process will run whenever the
'PlayerJoinEvent' is triggered.*/
}
```
Due to processes being asynchronous, they cannot have return values.<br>
If a process is subscribed to an event, it cannot take an input.
