ChatGPT CLI
===========

A command-line interface (CLI) for interacting with OpenAI's ChatGPT using the `chatgpt_rs` library.

Features
--------

*   Send messages and receive responses from ChatGPT in a conversational manner.
*   Save, load, and manage conversation history.
*   Supports various commands for managing conversations, such as `flush`, `save`, `load`, and `clear`.
*   Ask GPT to work with files via the CLI

Requirements
------------

*   Rust 1.56.0 or later
*   An OpenAI API key

Installation
------------

1.  Clone the repository:

    ```
    git clone https://github.com/your_username/chatgpt_cli.git
    ```
3.  Change to the project directory:

    ```
    cd chatgpt_cli
    ```
5.  Compile the project:

    ```
    cargo build --release
    ```
7.  (Optional) Add the compiled binary to your system's PATH for easier access.

Usage
-----

To run the ChatGPT CLI, execute the following command, replacing `your_api_key` with your OpenAI API key:

    ./target/release/chatgpt_cli your_api_key

You can also pass your prompt directly after the api key

    ./target/release/chatgpt_cli your_api_key write a haiku

You can interact with ChatGPT by typing messages directly in the CLI. The following commands are also available:
- `help`: Displays help message
- `flush`: Clears the current conversation
- `save [name]`: Saves the current conversation under the specified name
- `remove [name]`: Removes a saved conversation
- `load [name]`: Loads a saved conversation
- `clear`: Clears all saved conversations
- `list`: Lists all saved conversations
- `--file=[file(s)] --batch [optional, disable streaming process file(s) in batches] [message]`: Sends a message related to a file that is also uploaded
- `[message]`: Sends a message

Flags:
- `--gpt4`: Use this flag to enable GPT-4 model
- `--gpt35`: Use this flag to enable GPT-3.5 model

License
-------

This project is licensed under the [MIT License](LICENSE).
