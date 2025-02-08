Class Representative Voting System
A Django-based web application designed to manage and conduct class representative elections seamlessly. This project includes features for candidate registration, voter management, online voting, and displaying results. Additionally, QR code scanning is implemented using pyzbar to ensure secure voter authentication.

Features
Candidate Registration:

Candidates can register themselves for the election through a user-friendly form.
Information includes candidate details and their profile pictures.
Voter Management:

Handles voter details, including their names, departments, and profile pictures.
Ensures secure voter identification through QR code scanning.
QR Code Scanning:

Uses the pyzbar library to scan and authenticate voter IDs.
Prevents unauthorized voting by verifying QR codes on voter IDs.
Voting System:

Provides a simple and secure interface for voting.
Ensures that each voter can cast only one vote.
Prevents multiple votes from the same individual.
Results Display:

Displays election results with real-time updates.
Results are accessible to all authorized users.
Media Management:

Stores candidate and voter images for reference and display.
Responsive Design:

Clean and minimalistic UI for a seamless user experience.
Directory Structure
r
Copy
Edit
sidd-38-class-rep-voting/
├── Pipfile               # Dependencies for the project
├── db.sqlite3            # SQLite database
├── manage.py             # Django management commands
├── OnlineFranchise/      # Main project settings and configuration
├── candidatereg/         # Candidate registration app
├── homepage/             # Homepage and main interface
├── media/                # Media files (e.g., candidate and voter images)
├── results/              # Results app for displaying election results
├── static/               # Static assets (CSS, images)
├── voter/                # Voter management app
├── voting/               # Voting system app
Installation
Clone the repository:

bash
Copy
Edit
git clone https://github.com/yourusername/sidd-38-class-rep-voting.git
cd sidd-38-class-rep-voting
Install dependencies: Ensure you have pipenv installed, then run:

bash
Copy
Edit
pipenv install
Run migrations:

bash
Copy
Edit
python manage.py makemigrations
python manage.py migrate
Run the development server:

bash
Copy
Edit
python manage.py runserver
Access the application:

While the development server is running, open the URL http://127.0.0.1:8000 in your browser to access the application locally.
Usage
Candidate Registration:

Navigate to the candidate registration page to register class representatives.
Voter Authentication:

Use the QR code scanning feature to validate voter identity before allowing them to vote.
QR code generation for IDs should be done prior to using the app (this functionality can be extended as needed).
Voting Process:

Voters can cast their votes through the voting page after authentication.
Each voter is restricted to voting only once to ensure fairness.
View Results:

Navigate to the results page to view the outcome of the elections.
QR Code Scanning with Pyzbar
This application uses the pyzbar library for scanning QR codes on voter IDs. The QR code scanning functionality is integrated with the voter app to ensure that only valid voters can participate in the election process.

Setting up Pyzbar
Ensure that pyzbar is installed in your environment:

bash
Copy
Edit
pip install pyzbar
For Linux systems, you may need to install the required libraries:

bash
Copy
Edit
sudo apt-get install libzbar0
The QR code scanner reads the encoded information from voter IDs and verifies their eligibility to vote.

Static and Media Files
Static files: CSS and images are stored in the static/ folder.
Media files: Candidate and voter images are uploaded to the media/ folder.
Apps Overview
candidatereg: Handles candidate registration forms and validations.
voter: Manages voter information and QR code authentication.
voting: Implements the voting mechanism.
results: Displays election results in a clear format.
homepage: Provides the landing page and base templates.
