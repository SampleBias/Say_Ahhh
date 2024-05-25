# Say_Ahhh
Prompt Injection Tool for Healthcare LLM Applications
# Prompt Injection Testing Tool

The Prompt Injection Testing Tool is a Python script designed to assess the security of your AI system's prompt handling against a predefined list of user prompts commonly used for injection attacks. This tool utilizes the LLM XXX model to generate responses to system-user prompt pairs and outputs the results to a CSV file for analysis.

First Committ

## How It Works

The script takes as input a system prompt content, a file containing user prompts, and various configuration parameters. It then iterates over each user prompt, combines it with the system prompt, and sends the prompt pair to the OpenAI API for response generation. The generated responses are recorded along with the corresponding prompts in a CSV file for further examination.

+------------------------+
|      Configuration     |
| - API key              |
| - System prompt        |
| - User prompts file    |
| - Output CSV file      |
| - API temperature      |
| - API URL              |
+-----------+------------+
            |
            v
+-----------+------------+
| Read user prompts from |
|       text file        |
+-----------+------------+
            |
            v
+-----------+------------+
| Prepare payload with   |
| system and user messages|
+-----------+------------+
            |
            v
+-----------+------------+
|   Send POST request    |
|    to OpenAI API       |
+-----------+------------+
            |
            v
+-----------+------------+
|   Handle response      |
+-----------+------------+
            |
            v
+-----------+------------+
| Write response to CSV  |
|         file           |
+-----------+------------+
            |
            v
+-----------+------------+
|  Error handling (if any)|
+------------------------+

## Usage

1. **Prerequisites**: Before using the script, ensure you have obtained an API key from OpenAI and have Python installed on your system.

2. **Configuration**: Open the script file (`prompt_injection_testing.py`) and configure the following parameters:
   - `api_key`: Your OpenAI API key.
   - `system_prompt_content`: The content of the system prompt.
   - `user_prompts_file`: The path to the file containing user prompts (one prompt per line).
   - `output_csv_file`: The path to the output CSV file where the test results will be saved.
   - `api_temperature`: The temperature parameter for response generation (adjust as needed).

3. **Execution**: Run the script by executing the command `python prompt_injection_testing.py` in your terminal or command prompt.

4. **Analysis**: Once the script completes execution, review the generated CSV file (`prompt_test_results.csv`) to analyze the responses and identify any potential vulnerabilities in your AI system's prompt handling.

## Example Usage
Terminal:
python testingtool.py


## Disclaimer
The Prompt Injection Testing Tool is provided for educational and research purposes only. It should be used responsibly and in compliance with applicable laws and regulations. The authors do not accept any liability for any damages or losses resulting from the use of this tool.


## License
This project is licensed under the MIT License.
