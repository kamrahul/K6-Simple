# K6-Simple
 K6 Load testing script


# Install in mac

## Install brew :
### Step 1 : 
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
### Step 2 : 
- Add Homebrew to your PATH in ~/.zprofile:
### Step 3 :
  eval $(/opt/homebrew/bin/brew shellenv)
#### Step 4 :
  installation using query :    brew install k6

#### Step 5 :
Check installation : k6 Version



# Docker compose 

docker compose up will run the tests/basic_k6_test.js and load results to prometheus and can be visualized in grafana

# Settings in Grafana

You can access Grafana by going to localhost:4000. Initially, it will ask you to login, the username & password are both admin. Because we mapped the named volume, you will only need to do this once. When you are in the Grafana main menu, go to Configuration > Data source > add data source and find Prometheus

Once Prometheus is selected, you will need to add more data to the data source. Use http://prometheus:9090 as URL, this is defined in the prometheus.yml


Then at the bottom you can see if the data source works by clicking “Save and test”

# K6 Common commands 
 >  K6 version -> to get version number 
 > k6 help --> List all help commands
 > k6 run <path of js file>  -> run the test