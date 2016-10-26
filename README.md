

<!DOCTYPE html>
<html lang="en">
  <head>
    <title>Rock, paper, scissors</title>
  </head>
  <body>
    
    <!-- start body-->
    
    <h1>Rock, paper, scissors</h1>
      
      <a href="#" onclick="doTurn ('rock');"> choose rock</a><br>
      <a href="#" onclick="doTurn ('paper'); ">choose paper</a><br> 
      <a href= "#" onclick="doTurn ('scissors'); ">choose scissors</a><br>
    <div id="output">      </div>

    <!--end body -->
    
    
    
    <script>
      /* TODO: 
        -user input DONE kind of.
        -score increments
        -add output other than console
        -move script to external file
      */

      // string variables to hold possible choices
      // we'll use these later on
      var choice1 = "rock";
      var choice2 = "paper";
      var choice3 = "scissors";

      // number variables to hold the scores
      var humanScore = 0;
      var computerScore = 0;
      
      // string variables to hold the choices
      var humanChoice = "";
      var computerChoice = "";
      
      // variable to hold our output
      var output = "";
            
      function doTurn(humanChoice) {
         computerChoice = "rock"; // try changing these values to test!
         
         if (humanChoice === computerChoice) { // Draw
            console.log("Draw!");
            output = "Draw!";
         }
         else if ((humanChoice === "rock" && computerChoice === "scissors") ||
                 (humanChoice === "scissors" && computerChoice === "paper") ||
                 (humanChoice === "paper" && computerChoice === "rock")) { 
                 // Human won
            console.log("You win!"); 
            output = "You win!";
             humanScore= humanScore +1; //increment human score by 1 
         }
         else { // Human lost--no need to check by process of elimination
            console.log("You lose!");
            output = "You lose!";
              computerScore = computerScore + 1
         }
         
         document.getElementById("output").innerHTML = output;
      }
      
      
    </script>
    
  </body>
