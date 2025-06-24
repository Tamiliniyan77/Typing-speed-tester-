# Typing-speed-tester-
import time

# Sample text for typing test
test_text = "The quick brown fox jumps over the lazy dog."

print("Welcome to the Typing Speed Tester!")
print("Type the following sentence as fast and accurately as you can:")
print("\n>>", test_text)
input("\nPress Enter when you're ready to start...")

# Record start time
start_time = time.time()

# Get user input
typed_text = input("\nStart typing below:\n")

# Record end time
end_time = time.time()

# Calculate time taken in seconds
time_taken = end_time - start_time

# Calculate words per minute
word_count = len(typed_text.split())
wpm = (word_count / time_taken) * 60

# Calculate accuracy
correct_chars = sum(1 for i, c in enumerate(typed_text) if i < len(test_text) and c == test_text[i])
accuracy = (correct_chars / len(test_text)) * 100

# Show results
print("\n--- Results ---")
print(f"Time taken: {time_taken:.2f} seconds")
print(f"Words typed: {word_count}")
print(f"Typing Speed: {wpm:.2f} WPM")
print(f"Accuracy: {accuracy:.2f}%")
