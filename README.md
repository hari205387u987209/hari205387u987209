import random

# Define a dictionary of responses
responses = {
    "hello": ["Hello!", "Hi there!", "Hey!"],
    "how are you": ["I'm good, thanks!", "I'm doing well.", "I'm fine, how about you?"],
    "what's your name": ["I'm a chatbot.", "You can call me ChatGPT.", "I don't have a name."],
    "bye": ["Goodbye!", "See you later!", "Have a great day!"],
    "default": ["I'm not sure what you mean.", "Could you please rephrase that?", "I don't understand."],
}

def chatbot_response(user_input):
    # Convert user input to lowercase for case-insensitive matching
    user_input = user_input.lower()

    # Check if the user input matches any predefined keywords
    for key in responses:
        if key in user_input:
            return random.choice(responses[key])

    # If no keyword matches, return a default response
    return random.choice(responses["default"])

# Main loop for chatting
print("Chatbot: Hello! Type 'bye' to exit.")
while True:
    user_input = input("You: ")
    if user_input.lower() == "bye":
        print("Chatbot: Goodbye!")
        break
    response = chatbot_response(user_input)
    print("Chatbot:", response)


<!---
hari205387u987209/hari205387u987209 is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
