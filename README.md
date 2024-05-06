## Deep Analysis of WhatsApp Group Chat

This project analyzes a WhatsApp group chat based on its chat history stored in `_chat.txt`. It aims to answer various questions and provide insights into user behavior within the chat.

**Note:**

* This analysis is specific to chat history exported from an iOS device. Android devices and future iOS versions might require adjustments due to potential differences in chat storage formats and encryption methods.
* The analysis is based on a version relevant to 2023. Feel free to contribute to updates to accommodate changes in chat formats.

### Data Cleaning and Preprocessing

1. **Reading and Cleaning Chat Data:**
   - The chat transcript is read from `_chat.txt`.
   - Newline characters (`\n`) are replaced with spaces to separate messages.
   - Square brackets (`[]`) are replaced with newlines to differentiate timestamps and messages.

2. **Converting Data to DataFrame:**
   - The cleaned chat data is loaded into a pandas DataFrame (`df`).

3. **Extracting Message Components:**
   - The DataFrame is split into separate columns for `Date`, `Time`, `Member` (sender name), and `Message` content using string manipulation techniques.

4. **Handling Missing Values:**
   - Rows with missing messages are identified and dropped from the DataFrame (`final_df`).

5. **Identifying Missing Columns (Optional):**
   - This step involves analyzing the chat data to determine if any relevant information is missing from the extracted columns (`Date`, `Time`, `Member`, `Message`). Examples of potentially missing columns include:
     - `Media`: This column could indicate the presence of media attachments (images, videos, etc.) in the chat.
     - `Reaction`: This column could capture emoji reactions attached to messages.
     - **Custom Columns**: Depending on the specific analysis goals, you might want to extract additional information from messages, such as sentiment scores or named entities.

   - If missing columns are identified, the data cleaning and extraction steps can be adapted to incorporate them into the DataFrame.


### Uncovering Group Chat Trends

This analysis addresses a range of questions to provide a comprehensive understanding of the group chat:

* **Latest Polls:** Identify the five most recent polls conducted within the group.
* **Word Cloud:** Generate a visualization that highlights the most frequently used words, offering a glimpse into the group's vocabulary and potential topics.
* **Most Active User:** Determine the member who contributes the most messages to the chat, indicating their level of engagement.
* **Activity Patterns:**
    * **Most Active Hour:** Discover the hour of the day when chat activity peaks, providing insights into group members' typical communication schedules.
    * **Most Active Day of the Week:** Identify the weekday with the highest volume of messages, revealing potential patterns in group communication.
    * **Most Active Day Month-Wise:** Uncover the month with the most chat activity, indicating possible seasonal trends or events that influence group communication.
* **Group Sentiment:** Analyze the overall sentiment of the group using sentiment analysis techniques.  This can reveal the general mood and atmosphere within the chat.
* **Reasons for Leaving:** Explore messages containing the word "left" or similar phrases to understand why members might have departed from the group.
* **Sentiment of Leaving Members:** Analyze the sentiment of messages sent by members before leaving the group, potentially offering clues about their reasons for departure.
* **Identifying Negative Messages:** Pinpoint messages classified as negative based on sentiment analysis. This can help address potential issues within the group.

This in-depth analysis equips you with valuable insights into the group chat's dynamics, user behavior, and potential areas for improvement.
