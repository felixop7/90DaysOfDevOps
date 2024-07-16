# Day 13: Python Libraries for DevOps

## Daily Log

**Date:** July 1, 2024

Today's focus was on exploring essential Python libraries that DevOps engineers commonly use for parsing files and automating tasks. Understanding how to work with different file formats such as JSON and YAML is crucial for managing configurations and data in various DevOps scenarios.

## Key Concepts

### Reading JSON and YAML in Python

As a DevOps Engineer, being able to parse and manipulate different file formats is essential. Python provides robust libraries such as `json` and `yaml` for handling these tasks efficiently.

## Tasks

### 1. Create a Dictionary in Python and write it to a JSON file

#### Example:

```python
import json

# Create a dictionary
data = {
    "name": "DevOps Task",
    "description": "This is a task to demonstrate JSON handling in Python.",
    "completed": False
}

# Write the dictionary to a JSON file
with open('task.json', 'w', encoding='utf-8') as f:
    json.dump(data, f, ensure_ascii=False, indent=4)
```

### 2. Read a JSON file `services.json` kept in this folder and print the service names of every cloud service provider

#### services.json:

```json
{
  "services": {
    "debug": "on",
    "aws": {
      "name": "EC2",
      "type": "pay per hour",
      "instances": 500,
      "count": 500
    },
    "azure": {
      "name": "VM",
      "type": "pay per hour",
      "instances": 500,
      "count": 500
    },
    "gcp": {
      "name": "Compute Engine",
      "type": "pay per hour",
      "instances": 500,
      "count": 500
    }
  }
}
```

#### Example:

```python
import json

# Read the JSON file
json_file = "services.json"
with open(json_file, 'r', encoding='utf-8') as f:
    json_data = json.loads(f.read())

# Print the service names of every cloud service provider
print("Service Names:")
print(f"aws: {json_data['services']['aws']['name']}")
print(f"azure: {json_data['services']['azure']['name']}")
print(f"gcp: {json_data['services']['gcp']['name']}")
```

### 3. Read YAML file using Python, file `services.yaml` and read the contents to convert YAML to JSON

#### services.yaml:

```yaml
---
services:
  debug: "on"
  aws:
    name: EC2
    type: pay per hour
    instances: 500
    count: 500
  azure:
    name: VM
    type: pay per hour
    instances: 500
    count: 500
  gcp:
    name: Compute Engine
    type: pay per hour
    instances: 500
    count: 500
```

#### Example:

```python
import yaml
import json

# Read the YAML file
yaml_file = "services.yaml"
with open(yaml_file, "r") as stream:
    try:
        yaml_data = yaml.safe_load(stream)
    except yaml.YAMLError as exc:
        print(exc)

# Convert YAML data to JSON
json_data_from_yaml = json.dumps(yaml_data, indent=4)

print("Converted YAML to JSON:\n", json_data_from_yaml)
```

### parser.py:

```python
import json
import yaml

json_file = "services.json"
yaml_file = "services.yaml"

# Read JSON file
with open(json_file, 'r', encoding='utf-8') as f:
    json_data = json.loads(f.read())

print("JSON:\n", json_data)

# Read YAML file
with open(yaml_file, "r") as stream:
    try:
        yaml_data = yaml.safe_load(stream)
    except yaml.YAMLError as exc:
        print(exc)

print("YAML:\n", yaml_data)
```

## Reflection

Today's tasks reinforced my understanding of how to work with JSON and YAML files using Python. These skills are essential for automating configuration management and data processing tasks in a DevOps environment. The ability to parse and manipulate various file formats allows for more flexible and efficient automation scripts.

### References:

- [Python Official Documentation](https://docs.python.org/3/)
- [Python By Project](https://www.youtube.com/playlist?list=PLlfy9GnSVerSzFmQ8JqP9v0XHHOAeWbjo)

---

**Happy Learning! 🚀**

Roshan Sahani

---
