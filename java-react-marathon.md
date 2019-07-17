## Getting Started

```no-highlight
et get java-react-marathon
cd java-react-marathon
createdb java_react_marathon_development
idea .
```

## Avengers Assemble

You are the leader of S.H.I.E.L.D (Spring Hibernate Intelligence Exception Lombak Development ) and have been tasked with putting together a team of the most powerful Spring and React developers to battle the Mighty Python and his Ruby legion.

You have been given the migration to create your table, and the model for the characteristics necessary for a hero. The rest is up to you.

### Create Your Table

```no-highlight
As the leader of S.H.I.E.L.D
I want to have a roster of powered individuals
So that I can choose who to recruit
```

Acceptance Criteria:

- Create a seeder file with at least 5 characters
  - ensure at least 3 heroes and 2 non-heroes are present

### Create Your API

```no-highlight
As the leader of S.H.I.E.L.D
I want to be able to let the public report new powered characters
So that I can scout them for my team
```

Acceptance Criteria:
- Create a CharactersRepository which extends the `PagingAndSortingRepository`
- Create a RestController for your characters
- You should have an endpoint which allows creation of new characters
- visiting `/api/v1/characters` should display a JSON of your characters
- visiting `/api/v1/characters/{id}` should display a JSON for the character with the matching ID
- ensure that the show endpoint has error handling and results in a 404 if the character is not found

<!-- ### Create Your Repository

```no-highlight
As the leader of S.H.I.E.L.D
I want to share my characters with the world
So I can ensure the world knows who their heroes are
```

Acceptance Criteria:


- Create a Controller to handle request mapping for get requests to `characters/new` and `characters/index`  -->

### Create Your Character via React Form

Thus far all your preparation has been in Java. But we need this this to react faster than that... wait! We can use React.js for that.

```no-highlight
As the leader of S.H.I.E.L.D
I want to display my current list to the world
So that they know which individuals we are already aware of
```

- Create a container which Fetches the list of existing Characters via the RestAPI Controller we created earlier
- Only the characters' aliases and heroic status must be displayed
- The list of characters should be maintained in state
- The page should contain a link to a form to add a new Character

```no-highlight
As a concerned citizen
I want to be able to enter new characters via a form
To report emerging powered individuals
```

- Create a React form to allow for creation of new Characters
- Ensure all entity fields are present
- Age is the only non-required field

```no-highlight
As a concerned citizen
I want to be able to send my created character to S.H.I.E.L.D
So their list is up to date
```

- Create a React Fetch Post method to deliver the form data to the backend
- Ensure that a properly completed form persists the character in the database
- Redirect the user to the list of heroes. The new character should be present
