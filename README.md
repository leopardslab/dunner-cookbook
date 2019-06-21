# dunner-cookbook

A collection of Dunner recipes, which can be used as templates during initialization on [Dunner](https://github.com/leopardslab/dunner) in a project.

## Cookbook Structure

```
dunner-cookbook
└──recipes
	└── <recipe_name>
		└── <.dunner.yml>
		└── <metadata.yml>
	└── <recipe_name>
		└── <.dunner.yml>
		└── <metadata.yml>
```

## How to add your Dunner recipe?

Create us a pull request with your dunner task file in the structure as shown above. 
* The `recipes` folder contain a directory which is used as the name of recipe, with no spaces in the name, e.g. `go_github_release`. 
* `.dunner.yml` file inside recipe folder should define the docker tasks, well documented.
* Every recipe should have a `metadata.yml` which describes the recipe, with `name`, `description`, `version`, `preInstallCmd` and `postInstallCmd` values set.

A sample dunner task file: 

```yaml
deploy:
- image: 'emeraldsquad/sonar-scanner'
  commands:
  - ['sonar', 'scan']
- image: 'golang'
  commands:
  - ['go', 'install']
- image: 'mesosphere/aws-cli'
  commands:
  - ['aws', 'elasticbeanstalk update-application --application-name myapp']
  envs:
   - AWS_ACCESS_KEY_ID=`$AWS_KEY`
   - AWS_SECRET_ACCESS_KEY=`$AWS_SECRET`
   - AWS_DEFAULT_REGION=us-east1
- follow: 'status' #This refers to another task and can pass args too
  args: 'prod'
status:
- image: 'mesosphere/aws-cli'
  commands:
  - ['aws', 'elasticbeanstalk describe-events --environment-name $1']
  # This uses args passed to the task, `$1` means first arg
  envs:
   - AWS_ACCESS_KEY_ID=`$AWS_KEY`
   - AWS_SECRET_ACCESS_KEY=`$AWS_SECRET`
   - AWS_DEFAULT_REGION=us-east1
```