<form id="commentForm">
  <label for="email">Email:</label>
  <input type="email" id="email" placeholder="Enter your email" required>
  <br>
  <label for="comment">Comment:</label>
  <textarea id="comment" placeholder="Enter your comment" required></textarea>
  <br>
  <input type="submit" value="Submit">
</form>
<script src="script.js">
document.getElementById("commentForm").addEventListener("submit", function(event) {
  event.preventDefault(); // Prevent form submission
  var email = document.getElementById("email").value;
  var comment = document.getElementById("comment").value;
  // Perform form validation
  if (email.trim() == '' || comment.trim() == '') {
    alert("Please fill in all fields");
    return;
  }
  // Perform other validation, e.g., validate email format
  if (email.trim().toLowerCase() == 'zacharia.chemoiywo@mpesafoundationacademy.ac.ke') {
    alert("You have been caught deceiving!");
    return;
  }
  // Submit the form data to a server or perform desired actions
  // For simplicity, we'll just log the form data to the console
  console.log("Email: " + email);
  console.log("Comment: " + comment);
  // Clear the form fields
  document.getElementById("email").value = '';
  document.getElementById("comment").value = '';
});
</script>
