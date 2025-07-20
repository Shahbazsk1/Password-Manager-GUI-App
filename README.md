# Password-Manager-GUI-App
<h2>This app securely generates, stores, and retrieves passwords for different websites using a user-friendly GUI. It helps users manage multiple credentials with minimal effort.</h2>
<h3>Modules Used:</h3>
<ul>
  <li><b>tkinter :</b>	For building GUI elements: labels, buttons, entries, canvas, etc.</li>
  <li><b>random :</b>	For generating randomized passwords using choice, randint, shuffle</li>
  <li><b>json :</b>	To save and read data in .json format</li>
  <li><b>tkinter.messagebox :</b>	To show pop-up messages and error handling dialogs
</li>
</ul>
<h3>Code Breakdown</h3>
<h4>🧪 1. Password Generator</h4>
<ul>
  <li>Randomly picks:
    <ul>
      <li><b>8–10 letters</b></li>
      <li><b>2–4 symbols</b></li>
      <li><b>2–4 numbers</b></li>
    </ul>
  </li>
  <li>Combines and shuffles them</li>
  <li>Joins into a single password</li>
  <li>Inserts it into the GUI password entry</li>
  <li>Copies it to clipboard using pyperclip.copy(password)</li>
</ul>
<h4>💾 2. Save Passwords</h4>
<ul>
  <p>def save():</p>
  <ul>
    <li>Collects website, email, and password inputs</li>
    <li>Saves them as:
      <p>
        {
          "example.com": {
          "email": "shahbaz@gmail.com",
          "password": "p@ss123!"
        }
      }
      </p>
    </li>
    <li>If file doesn’t exist: creates it</li>
    <li>If file exists: updates the existing data</li>
    <li>Clears the form fields after saving</li>
  </ul>
</ul>
<h4>🔍 3. Find Password</h4>
<p>def find_password():</p>
<ul>
  <li>Searches data.json for the input website</li>
  <li>If found: displays email & password in a popup</li>
  <li>If not: shows "No details found" error</li>
</ul>
<h4>🖼 4. GUI (UI Setup)</h4>
<ul>
  <li><b>Canvas :</b>	Displays the logo image (logo.png)</li>
  <li><b>Label :</b>	Website, Email/Username, and Password labels</li>
  <li><b>Entry :</b>	Input fields for website, email, password</li>
  <li><b>Button :</b>	Search, Generate Password, Add credentials</li>
</ul>
<p>plaintext

┌──────────────────────────────────────┐
│           [ Logo Image ]             │
│ Website:  [_#website name_] [Search] │
│ Email:    [_#your email_]            │
│ Password: [#enter pass] [Generate..] │
│           [       Add             ]  │
└──────────────────────────────────────┘
</p>
<h3>🚀 How to Run the Project</h3>
<ol>
  <li>Save the code in a file named password_manager.py</li>
  <li>Add an image named logo.png (200x200 preferred) in the same directory</li>
  <li>Install dependencies:
    <p>pip install pyperclip</p>
  </li>
  <li>Run the file:
    <p>python password_manager.py</p>
  </li>
</ol>
