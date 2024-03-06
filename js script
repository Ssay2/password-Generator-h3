var generateBtn = document.querySelector("#generate");

// Add event listener to generate button
generateBtn.addEventListener("click", writePassword);

// Function to generate password
function generatePassword() {
  var lowercaseLetters = "abcdefghijklmnopqrstuvwxyz";
  var uppercaseLetters = "ABCDEFGHIJKLMNOPQRSTUVWXYZ";
  var numbers = "0123456789";
  var specialCharacters = "!@#$%^&*()_+~`|}{[]\:;?><,./-=";

  var length = prompt("Enter the length of the password (between 8 and 128):");
  length = parseInt(length);
  if (isNaN(length) || length < 8 || length > 128) {
    alert("Invalid length. Password length must be between 8 and 128 characters.");
    return;
  }

  var includeLowercase = confirm("Include lowercase letters?");
  var includeUppercase = confirm("Include uppercase letters?");
  var includeNumbers = confirm("Include numbers?");
  var includeSpecialCharacters = confirm("Include special characters?");

  if (!includeLowercase && !includeUppercase && !includeNumbers && !includeSpecialCharacters) {
    alert("You must select at least one type of character to include.");
    return;
  }

  var characters = "";
  if (includeLowercase) {
    characters += lowercaseLetters;
  }
  if (includeUppercase) {
    characters += uppercaseLetters;
  }
  if (includeNumbers) {
    characters += numbers;
  }
  if (includeSpecialCharacters) {
    characters += specialCharacters;
  }

  var password = "";
  for (var i = 0; i < length; i++) {
    password += characters.charAt(Math.floor(Math.random() * characters.length));
  }

  return password;
}

// Function to write password to the #password input
function writePassword() {
  var password = generatePassword();
  if (password) {
    var passwordText = document.querySelector("#password");
    passwordText.value = password;
  }
}
