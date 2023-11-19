# chatbot
import random

def get_response(user_input):
    user_input = user_input.lower()

    # Define some basic rules for responses
    if "hello" in user_input:
        return "Hi there! How can I help you?"
    elif "how are you" in user_input:
        return "I'm just a computer program, but thanks for asking!"
    elif "bye" in user_input:
        return "Goodbye! Have a great day."
    else:
        return "I'm not sure how to respond to that. Ask me something else."

def chatbot():
    print("Chatbot: Hello! Type 'bye' to exit.")

    while True:
        user_input = input("You: ")
        
        if user_input.lower() == 'bye':
            print("Chatbot: Goodbye!")
            break

        response = get_response(user_input)
        print("Chatbot:", response)

if __name__ == "__main__":
    chatbot()
