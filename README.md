# **Medical Policy Extractor**

## **Overview**

The `Medical Policy Extractor` project is designed to extract and analyze medical necessity policies to identify ICD-10, CPT, and HCPCS procedure and diagnosis codes. The tool parses policy documents and extracts relevant information about procedures and diagnoses, marking whether they are medically necessary based on insurer policies.

The project is implemented as a Jupyter notebook (`.ipynb` file) and Gradio App where various functions have been defined to scrape, extract, and transform policy data.


## Requirements

You can install all dependencies by running:

```bash
pip install -r requirements.txt
```


## Installation

1. Clone the repository:

    ```bash
    git clone https://github.com/benz3927/Medical-Policy-Extractor.git
    cd Medical-Policy-Extractor
    ```

2. Create and activate a virtual environment:

    ```bash
    python3 -m venv .venv
    source .venv/bin/activate  # For Windows, use .venv\Scripts\activate
    ```

3. Install dependencies:

    ```bash
    pip install -r requirements.txt
    ```


## Usage

### 1. Extracting Policy Information

In the Jupyter notebook, you can use functions to extract key information from medical necessity policies.

#### Example: Extract Basic Information

Use the `get_basic_info` function to extract basic details from the first paragraph of a policy.

```python
first_paragraph = "..."
basic_info = get_basic_info(first_paragraph)
print(basic_info)
```

### Example Output

The final output will consist of a DataFrame with columns such as:

- `Procedure`: The procedure code (e.g., CPT, ICD-10)
- `Diagnosis`: The diagnosis code (e.g., ICD-10)
- `SessionNum`: The session number
- `MedNecessityIdx`: Medically necessary indicator (`1: Medically Necessary`, `0: Not Medically Necessary`, or `-1: Unclear`)

## Hugging Face Space

You can also use the tool through the following Hugging Face Space:  
[Extract Medical Policies on Hugging Face](https://huggingface.co/spaces/bzhao3927/Extract_Medical_Policies).

## Contributing

Feel free to fork the project and submit pull requests. We welcome contributions from the community.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
