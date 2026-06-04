python -m venv dbt-learn 
-> creating virtual envirnoment in python 

activate the environment 
-> source dbt-learn/Scripts/activate

installing the packages 
-> pip install -r requirements.txt

export this env_dev
 export BIGQUERY_PROJECT="e-comas-data-engineering"

inside the answers folder run dbt deps (it will install the package)
have to run this command 
gcloud auth application-default login

 dbt run -s stg_ecommerce__orders --profiles-dir .


dbt init -> this command will create the new dbt template project 

dbt debug --config-dir -> it will give path of the profile.yml file of the current project

dbt run-operation generate_base_model  --args '{"source_name": "us_temp_ecommerce" , "table_name": "products}'

dbt run -s stg_ecommerce__orders

dbt run-operation generate_model_yaml --args '{"model_names": ["stg_ecommerce__orders"]}'

dbt test -s stg_ecommerce__orders   

dbt run && dbt test 