# MistyAI CloudArch Designer

MistyAI CloudArch Designer is a cloud architecture design tool built using Streamlit that allows developers to design cloud systems using various cloud providers such as AWS, Azure, Google Cloud, and others. The tool generates a visual representation of the architecture in PNG format and provides an option to export the design as a DrawIO file.

## Features

- **Authentication System:** Secure access to the app with session validation and access codes.
- **Cloud Provider Selection:** Choose from a range of cloud providers (AWS, Azure, Google Cloud, IBM Cloud, Oracle Cloud).
- **Cloud Resource Management:** Define the resources used, group them into clusters, and describe their relationships.
- **LLM Integration:** Uses a language model to assist with the generation of architecture diagrams.
- **Export Options:** Download generated cloud architecture diagrams as PNG or DrawIO files.
- **Idle Session Management:** Automatically terminate sessions and clean up resources if idle for more than 30 seconds.
- **Periodic Cleanup:** Automatically removes temporary files after a set interval to save storage.

## Getting Started

### Prerequisites

Before running the project, make sure you have the following installed:

- Python 3.8+
- [Streamlit](https://docs.streamlit.io/library/get-started/installation) (Install via `pip install streamlit`)
- Other required Python packages are listed in the `requirements.txt` file. You can install them using:
- 
  ```bash
  pip install -r requirements.txt
  ```
  
Installation

Clone the repository:

 ```bash
git clone https://github.com/your-username/mistyai-cloudarch-designer.git
cd mistyai-cloudarch-designer
  ```

Install the required dependencies:

 ```bash
pip install -r requirements.txt
 ```


Add your OpenAI and Google Cloud configurations in the config.py file (details below).

Place your authentication details in access_codes.json and session management in sessions.json.
Start the application:


 ```bash
streamlit run app.py
 ```

Configuration
Create a config.py file with your OpenAI and Google Cloud API details:

 ```bash
# config.py

def read_openai_config():
    return {
        "api_key": "your_openai_api_key",
        "other_config": "other_value"
    }

def read_google_cloud_config():
    return {
        "api_key": "your_google_cloud_api_key",
        "other_config": "other_value"
    }

 ```
Ensure your OpenAI, Google Cloud, or any other cloud provider configurations are correctly set up for generating architecture diagrams.

##Usage
- **Load Example Data: Click the Load Example Data button to pre-fill the form with a sample architecture.
  
- **Submit Custom Data: Fill in your own architecture details and click Submit to generate a diagram.
  
- **Regenerate Diagram: Use the Regenerate button to run a new inference and regenerate the architecture diagram.
  
- **Export to DrawIO: After generating the diagram, you can download the .drawio file for further editing.
  
- **Restart the Process: Click Restart to clean up all generated files and start fresh.
  

Cleanup - The app automatically deletes generated files after 30 minutes. You can also manually trigger a cleanup by pressing the Restart button, which removes all associated files for the session.


Sessions - The session system ensures that a user is logged in and authenticated. The session expires after 30 minutes of inactivity. After that, the user must re-authenticate.


Contributing - We welcome contributions! Feel free to open an issue or submit a pull request for any bugs, features, or improvements. Ensure you follow the best practices:


Fork the repository - Create your feature branch:


For any questions, feel free to join our Discord Community.



##Happy Contributing! 🚀
