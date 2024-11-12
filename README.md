# zentn-chat-archive


Here are the complete rules for the .zentn format along with examples:

### .zentn Format Rules:
1. **Chat Structure**:
   - Each chat is represented by `List.obj.X("ChatName")`, where `X` is an index starting from 1.
   - Each object represents a single chat.

   **Example**:
   ```
   List.obj.1("Chat1")
   ```

2. **Attributes**:
   - Attributes are defined using two spaces for indentation, formatted as `Identifier = "Message"`.
   - The `Identifier` can be `Host`, `Client`, or any custom name. 
   - `Message` is the text content of that identifier.

   **Example**:
   ```
   List.obj.1("Chat1")
     Host = "Hello, how are you?"
     Client = "I'm doing well, thanks! How about you?"
   ```

3. **Multiple Messages**:
   - Multiple messages are allowed within a single chat object.
   - Messages are added sequentially under the object declaration.

   **Example**:
   ```
   List.obj.2("Chat2")
     User1 = "Good morning!"
     User2 = "Morning! Ready for the meeting?"
     User1 = "Yes, let's do this."
   ```

4. **Escaping Inner Quotes**:
   - Double quotation marks inside a message should be escaped with `""` to preserve them.

   **Example**:
   ```
   List.obj.3("Chat3")
     Host = "He said, ""Let's meet at noon."" and I agreed."
   ```

5. **End of Chat**:
   - Each chat group is separated by a newline. Each chat object (`List.obj`) starts a new chat.

   **Example**:
   ```
   List.obj.4("Chat4")
     UserA = "Did you finish the project?"
     UserB = "Almost, just final touches left."

   List.obj.5("Chat5")
     UserA = "Great, can't wait to see it!"
   ```

6. **Custom Identifiers**:
   - You can use custom identifiers beyond `Host` and `Client`.

   **Example**:
   ```
   List.obj.6("TeamDiscussion")
     Leader = "Let's start the brainstorming session."
     Member1 = "I have an idea about improving the UI."
     Member2 = "That's a good point, we should explore it."
   ```

### Full .zentn Example:
```
List.obj.1("ProjectUpdate")
  Manager = "How's the progress on the main task?"
  Developer = "We're about 80% done. Should be finished by tomorrow."
  Manager = "Perfect, keep me posted."

List.obj.2("FeedbackSession")
  Leader = "Any feedback on the new workflow?"
  Member1 = "It's much smoother now, thanks for implementing the changes."
  Member2 = "I agree, it's definitely more efficient."
```

These examples and rules should help you build or interpret .zentn files.
