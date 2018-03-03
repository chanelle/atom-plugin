# Atom Plugin
The Atom Plugin is designed to help with service discover and Storyscript debugging.

Below are a list of core features.

### Right Panel
This full-height panel is designed for service discovery.
Users can search for services in the Asyncy Hub and get
details and documentations about the service.

**Initial State**
- Welcome branding and illustration
- User will be prompted to enter in their Hub token (not required)

**Natural State**
- Large search bar at the top (empty)
- List syntax errors, if any
- When the cursor has focus on a line which is a container
  - Pull up that containers details (Server State)

**Search State**
> Search bar is focused.

- A list of services appear filtered by the query.

**Service State**
> A single service is selected.

- Header image and avatar for the service
- Description of container (140 characters)
- List of command (clickable accordions)
  - Reveal details about the command (in/outs)

## Typing
Help the user complete each line by providing type-ahead assistance.

#### Assist Commands
When focus in on a container:

```
twitter
        [ tweet - Post a tweet     ]
        [ follow - Follow a user   ]
```
1. Show the service details in the Right Panel
2. Assist them with a list below the cursor of optional commands


#### Assist Arguments
When focus in on a container command:

```
twitter tweet [handler :string] [message :string]
              ^
         1. Show the service details in the Right Panel
         2. Drop down the specific command
         3. Assist them with argument blocks (as seen above at ^)

twitter tweet '@foobar' [message :string]
                        ^
```

#### Show Dictionary Values
When focus in on an object of type Dictionary:

```
dictionary.
           [ key1   ]
           [ key2   ]
```
> The objects keys will be listed below and autocompleted.


## Configuration
- Multiple Hub endpoints for on-premise customers
- API token to Hub
- Change panel location (left or right)
