How to run the application
--------------------------

To open locally on browser:
1) Double-click on '\frontend-nanodegree-mobile-portfolio\src\index.html' to open the page in your default browser and then navigate to other pages from there.

To open via internet (using ngrok):
1) Make sure ngrok is downloaded and up to date. For details, visit: https://ngrok.com
2) Make sure Python is downloaded and up to date. For details visit: https://python.org
3) In the command bar, change current directory to '...\frontend-nanodegree-mobile-portfolio\'
4) Using Python 3 syntax, open a simple http server in the command bar: 'python -m http.server 8000' (or another port other than '8000' if you'd like).
5) Test that this port is being served by opening with your browser 'http://localhost:8000'.
6) If your page appears, then in another command prompt type 'ngrok http 8000'. This will then display two urls, both of which can be used to navigate from the internet to your local server.

Optimizations in 'index.html'
-----------------------------

1) Reference print media query/stylesheet only on print
2) Execute google analytics js asynchronously
3) Reduce profilepic.gif image size
4) Reduce pizzeria.jpg image size
5) Remove link to fonts.googleapis since 'Open Sans' appears to be already available to the browser
6) Inline a portion of css content.

Optimizations in 'main.js'
--------------------------

1) Simply function determineDx by removing extraneous calculations
2) Move 'document.querySelectorAll' out of loop in function 'changePizzaSizes' so that this method isn't called with every loop iteration
3) Define 'document.body.scrollTop' as a variable  so that it doesn't need to be calculated with each loop iteration
4) Reduced number of pizzes rendered from 200 to 32 to ensure that enough pizzas are rendered to display 4 complete rows of 8 pizzas.
5) Reworked 'changePizzaSizes' function to change value of var 'newsize' so that pizza sizes are actually changed