# ppdg-extractor
Extract (CSV) codes from and screenshot (JPG) PayPal Digital Gifts gift cards. Adapted from https://github.com/stevenmirabito/ code in order to clean up screenshots, save screenshots as .JPG, and to process PIN and non-PIN cards using the same program.

Program specifically configured on Windows - includes ChromeDriver.exe - for gmail.

1) Install Python 3.6.1

2) Open command prompt (cmd) and navigate to this folder. Install the dependencies by running the following commands:
	
	 pip3 install -r requirements.txt

3) Edit config.py file:
	
	a) Change IMAP_USERNAME to your gmail account
	
	b) Change IMAP_PASSWORD to your gmail password
	
	c) Change XPATH locations for card_amount, card_number, and card_pin if necessary (will be required if these fields come back as N/A in the console. XPATH can be found by inspecting element in Chrome, right clicking on the item in the elements console, Copy, "Copy XPATH".
	
	d) Create a gmail label for the cards you would like to extract and change FOLDER to this label.
	
	e) Note: When logging in for the first time, gmail may block access. You will need to follow the steps in the email to follow to enable less secure applications.
	
4) Double click on MasterExtractor.bat to run the program. You will get .jpg screenshots in the "screenshots" folder and will have a .csv file with near GCW (GiftCardWiki) submission standards.

5) Enjoy!
