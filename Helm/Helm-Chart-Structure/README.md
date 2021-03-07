## Helm Chart Structure
**- my-first-chart:** It is the folder name and it content the name of the chart
**- chart.yml**: contents the information about the chart
**- Template:** It contents kubernetes objects definition files like deployment, serverce, configmap etc.
**- chart:** It contains a sub chart or dependency. If your chart has dependencies, you can add them in the chart folder
**- NOTES.txt:** It contents what is going to display on the terminal when someone download and install your chart or when you install the chart
**- README.md:** It is use to document the chart
**- varlues.yaml:** it has all the default configuration values for the chart
**- _helpers:** It contains functions. If we have a code that repeats itself many times in the code, we can create functions in -helpers and call those functions in the code. This will reduce duplicated lines of code in you manifest files
**- tests:** The content of this runs first before the actual deployment can happen. If the code in the test folder fails to run, your application will not be deployed in kubernetes. It is useful if you want to test something before deploying your application
**- .helmignore:** This is the same like dockerignore, gitignore etc or files that we don't want consider for Helm command