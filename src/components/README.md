# Import the required modules
import os
import sys

# Define the project metadata
project_name = "api-service"
project_version = "1.0.0"
project_description = "API service for interacting with external resources"

# Define the dependencies
dependencies = {
    "requests": "^2.27.1",
    "flask": "^2.0.2",
    "flask-restful": "^0.3.9"
}

# Define the development dependencies
dev_dependencies = {
    "pytest": "^6.2.4",
    "pytest-cov": "^2.12.1"
}

# Define the environment variables
env_variables = {
    "FLASK_ENV": "development",
    "FLASK_DEBUG": "1"
}

# Define the entry point
if __name__ == "__main__":
    # Check if the project directory is set as the current working directory
    if os.path.dirname(os.path.abspath(__file__))!= os.getcwd():
        print("Error: Project directory is not set as the current working directory.")
        sys.exit(1)

    # Print the project metadata
    print(f"Project name: {project_name}")
    print(f"Project version: {project_version}")
    print(f"Project description: {project_description}")

    # Print the dependencies
    print("Dependencies:")
    for dependency, version in dependencies.items():
        print(f"- {dependency}: {version}")

    # Print the development dependencies
    print("\nDevelopment dependencies:")
    for dependency, version in dev_dependencies.items():
        print(f"- {dependency}: {version}")

    # Print the environment variables
    print("\nEnvironment variables:")
    for variable, value in env_variables.items():
        print(f"- {variable}: {value}")