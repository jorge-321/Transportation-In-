# Transportation-In-
Students and adults who use public transportation on a daily bases need an efficient way to recharge their tap cards, pay their bus fee, as well as knowing at what time their bus is coming. 

<link href="file:///Users/macbookpro/Desktop/Screen%20Shot%202017-01-12%20at%2012.07.51%20PM.png" rel="stylesheet" type="text/css">
<style>
  .red-text {
    color: red;
  }

  h2 {
    font-family: Lobster, Monospace;
  }

  p {
    font-size: 16px;
    font-family: Monospace;
  }

  .thick-green-border {
    border-color: green;
    border-width: 10px;
    border-style: solid;
    border-radius: 50%;
  }

  .smaller-image {
    width: 100px;
  }
</style>

<h2 class="red-text">Pay N Flow App</h2>

<p>Click here for <a href="#">to Sin Up or Sin In</a>.</p>

<a href="#"><img class="smaller-image thick-green-border" alt="Pay N Flow Logo " src="https://www.innovationportal.org/file/download/389869"></a>

<p>How to Pay:</p>
<ul>
  <li>Log in</li>
  <li>Inserting card information </li>
  <li>Tap N Go!</li>
</ul>
<p>Top 3 things to do:</p>
<ol>
  <li>build security </li>
  <li>coustemrs trust</li>
  <li>facilitating payment</li>
</ol>
<input type="text">

<form action="/submit-cat-photo">
  <input type="text" placeholder="cat photo URL">
  <button type="submit">Submit</button>
</form>
/* Bonfire: Convert HTML Entities
Difficulty: 2/5
Convert the characters "&", "<", ">", '"' (double quote), and "'" (apostrophe), in a string to their
corresponding HTML entities.
Remember to use RSAP if you get stuck. Try to pair program. Write your own code.
Here are some helpful links:
RegExp HTML Entities
Code by Rafael Rodriguez
rafase282@gmail.com
http://www.freecodecamp.com/rafase282
*/

function convert(str) {
  // Split by character to avoid problems.

  var temp = str.split('');

  // Since we are only checking for a few HTML elements I used a switch

  for (var i = 0; i < temp.length; i++) {
    switch (temp[i]) {
      case '<':
        temp[i] = '&lt;';
        break;
      case '&':
        temp[i] = '&amp;';
        break;
      case '>':
        temp[i] = '&gt;';
        break;
      case '"':
        temp[i] = '&quot;';
        break;
      case "'":
        temp[i] = '&apos;';
        break;
    }
  }

  temp = temp.join('');
  return temp;
}

convert('Dolce & Gabbana');

// More advance Solution

function convert(str) {
  // Use Object Lookup to declare as many HTML entities as needed.
  htmlEntities={
    '&':'&amp;',
    '<':'&lt;',
    '>':'&gt;',
    '\"':'&quot;',
    '\'':'&apos;'
  };
  //Use map function to return a filtered str with all entities changed automatically.
  return str.split('').map(function(entity){
    return htmlEntities[entity] || entity;
  }).join('');
}
