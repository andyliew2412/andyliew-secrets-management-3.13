# Learn how to retrieve AWS secrets and parameters store value

1) Create a Github repository and clone locally.
2) Add repository secrets and variables for Github action to login AWS.
3) Create AWS secrets manager- Secrets and AWS System Manager – Parameter Store on AWS console.
4) Using AWS CLI command to retrieve secret key from AWS on local computer.

-      aws secretsmanager get-secret-value
        --secret-id <SECRET_NAME>
        --query SecretString
        --output json | jq -r '. | fromjson | .<Secret.Key>'
5) Using AWS CLI command to retrieve parameter store value from AWS on local computer.
-      aws ssm get-parameter
        --name <PARAMETER_NAME>
        --query <Parameter.Value>
        --output text
