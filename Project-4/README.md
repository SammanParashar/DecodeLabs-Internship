# Project 4 - AWS Lambda (Serverless Computing)

## Objective
Create an AWS Lambda function that accepts two numbers as input and returns their sum.

## AWS Services Used
- AWS Lambda
- Amazon CloudWatch

## Programming Language
- Python 3.13

## Function Code

```python
def lambda_handler(event, context):
    num1 = event.get("num1", 0)
    num2 = event.get("num2", 0)

    total = num1 + num2

    return {
        "Sum": total
    }
```

## Test Event

Input:

```json
{
  "num1": 15,
  "num2": 25
}
```

Output:

```json
{
  "Sum": 40
}
```

## Result
The AWS Lambda function executed successfully and the execution was verified using Amazon CloudWatch Logs.
