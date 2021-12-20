# robo-glad




// var playerName = window.prompt("What is your robot's name?");

// Note the lack of qoutation marks around playerName

//window.alert(playerName); <-- allowed player name to pop up.

// What is this?
//console.log(playerName);

//console.log("this logs a string, good for leaving yourself a message");

//this will do math and log 20
//console.log(10 + 10);

//what is this?
//console.log("Our robot's name is " + playerName);

// this creates a function named "fight"
//function fight() {
    //window.alert("The fight has begun!");
  //}

  // fight();


  var playerName = window.prompt("What is your robot's name?");
  var playerHealth = 100;
  var playerAttack = 10;
  var playerMoney = 10;

  // You can also log multiple values at once like this
  console.log(playerName, playerAttack, playerHealth);

  var enemyName = "Roborto";
  var enemyHealth = 50;
  var enemyAttack = 12;


    var promptFight = window.prompt("Would you like to FIGHT or Skip this battle? Enter 'FIGHT' or 'SKIP' to choose. ");

////Dont pay attention to this ////

    // if player choses to fight, then fight
    if (promptFight === "fight" || promptFight == "FIGHT") {
        // remove enemy's health by subtracting the amount set in the PlayerAttack variable
        enemyHealth = enemyHealth - playerAttack;
        console.log(
            playerName + " attacked " + enemyName + ". " + enemyName + " now has " + enemyHealth + " health remaining. "
        );
    
        // check enemy's health
        if (enemyHealth <= 0 ) {
            window.alert(enemyName + " has died!");
        } else {
            window.alert(enemyName + " still has " + enemyHealth + "health left. ");
        }

        // Remove player's health by subtracting the amount in the enemeyAttack variable
        playerHealth = playerHealth - enemyHealth;
        console.log(
            enemyName + " attacked " + playerName + ". " + playerName + "now has " + playerHealth + "health remaining."
        );
        
        // check player's health
    
        if (playerHealth <= 0) {
            window.alert(playerHealth + "has died!");
        } else {
            window.alert(playerName + "still has " + playerHealth + "health left. ");
        }
        // if player choses to skip
    } else if (promptFight == "skip" || promptFight == "SKIP") {
        // confirm player wants to skip
        var confirmSkip = window.confirm("Are you sure you'd like to quit?");

        // if yes (true), leave fight
        if (confirmSkip) {
            window.alert(playerName + "has decided to skip this fight. Goodbye!");
            // subtract money from playerMoney for skipping
            playerMoney = playerMoney - 2;
        }

        // if no (false), ask question again by running fight() again

        else {
            fight();
        }

        window.alert(playerName + " has chosen to skip the fight!");
    } else { window.alert("You need to chose valid option. Try again!");
    
}


/// pay attention to everything below ///


// create function
var fight = function() {
    // Alert players that they are starting the round
      window.alert("Welcome to Robot Gladiators!"); 
  
      // Subtract the value of `playerAttack` from the value of `enemyHealth` and use that result to update the value in the `enemyHealth` variable
      enemyHealth = enemyHealth - playerAttack;
      // Log a resulting message to the console so we know that it worked.
      console.log(
          playerName + " attacked " + enemyName + ". " + enemyName + " now has " + enemyHealth + " health remaining."
      );
      // Subtract the value of `enemyAttack` from the value of `playerHealth` and use that result to update the value in the `playerHealth` variable.
      playerHealth = playerHealth - enemyAttack;
  
      // Log a resulting message to the console so we know that it worked.
      console.log(
          enemyName + " attacked " + playerName + ". " + playerName + " now has " + playerHealth + " health remaining." 
      );
  
      //check player's health
      if (playerHealth <= 0) {
          window.alert(playerName + "has died!");
      }
      else {
          window.alert(playerName + " still has " + playerHealth + " health left.");
      }
  };
      // put new code under this 
      console.log (
          playerName + " attacked " + enemyName + ". " + enemyName + " now has " + enemyHealth + " health remaining."
      );
      
  
      // check enemy's health
      if (enemyHealth <= 0) {
          window.alert(enemyName + " has died!");
          }
          else {
              window.alert(enemyName + " still has " + enemyHealth + " health left.");
          }
  
  // execute function
  //  fight();