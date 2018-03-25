# Chat Commands  
Chat commands are bot capabilities that can be activated by users connected to the bot's server, as well as directly from the bot console application. Below is a list of all available commands, how they are used, and some examples.  
When reading syntax, please keep the following in mind:
 - Parameters with brackets `[ ]` are required.
 - Parameters with angled brackets `< >` are required and accept only a small set of values denoted in the parameters section.
 - Parameters with parentheses `( )` are optional.

## Dad Mode  
Controls Dad Mode functionality. When active, the bot will respond to any message that starts along the lines of "I'm [X]" with "Hi, [X]. I'm dad!"  
  
### Valid Syntaxes  
`!dadmode <action>`  

### Parameters  
Parameter Location | Value | Aliases | Description  
-------------------|-------|---------|------------  
action | 'enable' | 'on' | Activates Dad Mode.  
action | 'disable' | 'off' | Deactivates Dad Mode.  

### Example
```
User: !dadmode enable
Bot: Dad Mode has been activated.

```
  
## Idle Checker  
 Controls Idle Checker functionality. When active, the bot will automatically move inactive users to a designated AFK channel after reaching a time threshold.  

### Valid Syntaxes  
`!idlechecker <action>`  
`!idlechecker (status)`

### Parameters
Parameter Location | Value | Aliases | Description  
-------------------|-------|---------|------------  
action | 'enable' | 'on' | Activates Idle Checker.  
action | 'disable' | 'off' | Deactivates Idle Checker.  
status | 'status' | [empty] | Returns the current status of Idle Checker.  
  
### Example
```
User: !idlechecker on
Bot: Idle Check enabled. Idle users will now be automatically moved to "AFK" after 30 minutes.

User: !idlechecker
Bot: Idle Checker is currently active. Users will be moved to "AFK" after 30 minutes of inactivity.

User: !idlechecker status
Bot: Idle Checker is currently active. Users will be moved to "AFK" after 30 minutes of inactivity.

```

## Kick  
Forcefully disconnects a specified user from the server.

### Valid Syntaxes  
`!kick [client_id] [reason]`

### Parameters
Parameter Location | Value | Description  
-------------------|-------|------------  
client_id | Integer | The client ID of the user being kicked.  
reason | String | Justification used when kicking the user.  

### Example
```
User: !kick 3 Because I said so.
Server: UserWithId3 was kicked from the server by "Bot" (Because I said so.)

User: !kick 3 Do it again.
Bot: No user is currently connected using id: 3
```
  
## Ping/Pong  
Simple health-check command that has the bot return a simple phrase when messaged.

### Valid Syntaxes
`!ping`

### Example
```
User: !ping
Bot: Pong!
```