import random

# List of greetings and responses
greetings = ["hello", "hi", "hey", "greetings"]
responses = ["Hello!", "Hi there!", "Hey!", "Greetings!"]

# List of questions and responses
questions = ["how are you?", "how's it going?", "what's up?"]
question_responses = ["I'm doing great, thanks!", "I'm fine, how about you?", "Not much, just chatting with you!"]
questions = ["happy birthday", "how is your day?","how you enjoyed",]
question_responses = ["thanks!", "that's good", "i enjoyed a lot with my friends&family"]


# List of default responses
default_responses = ["I'm sorry, I didn't understand that.", "Could you please rephrase that?", "I'm still learning. Can you ask me something else?"]

# Function to generate a response to user input
def generate_response(user_input):
    user_input = user_input.lower()
    
    if user_input in greetings:
        return random.choice(responses)
    elif user_input in questions:
        return random.choice(question_responses)
    else:
        return random.choice(default_responses)

# Main conversation loop
print("Chatbot: Hello! How can I help you today?")
while True:
    user_input = input("User: ")
    if user_input.lower() == "bye":
        print("Chatbot: Goodbye!")
        break
    else:
        response = generate_response(user_input)
        print("Chatbot:", response)
