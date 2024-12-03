This repo is for helm practice.

Step 1 : Clone the repo.

Step 2 : Edit the values.yaml file under dev folder if required.

Step 3: Generate the yaml files using the helm chart. 
<br/> command : helm template -g --output-dir ./ymls . -f <name_of_the_value_yaml> -f <name_of_secret_file>
<br/> . : means current context
<br/> ./ymls : will be generated after execution of the above command

step 4: install the stack 

command : helm install <name_of_stack> -n <name_of_namespace> .-f <name_of_the_value_yaml> -f <name_of_secret_file> --create-namespace

step 5 : list of deployments 

helm ls -A
