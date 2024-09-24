<h1>ACME System Verify Account Positions</h1>
<p>This UiPath project automates a workflow that interacts with both the ACME System1 website and ACME System3 desktop application. It utilizes three custom libraries to streamline the process of extracting and updating work items from ACME System1 and searching for related data within ACME System3.</p>

<h2>Libraries Used</h2>
<p>This project uses the following custom libraries:</p>
<ul>
    <li><strong>Google Search Library:</strong> Handles the process of launching Google Chrome, searching for the ACME System1 website, and navigating to it.</li>
    <li><strong>ACME System1 Website Library:</strong> Automates interactions with the ACME System1 website (web automation).</li>
    <li><strong>ACME System3 Desktop Application Library:</strong> Automates operations within the ACME System3 desktop application (desktop automation).</li>
</ul>

<details><summary><h2>Process Workflow</h2></summary>
<ol>
    <li><strong>Open ACME System1 Website:</strong> 
        <ul>
            <li>Launches Google Chrome and opens the Google search page.</li>
            <li>Types "ACME System" in the search box and clicks the first search result to navigate to the ACME System1 website.</li>
        </ul>
    </li>
    <li><strong>Login to ACME System1 Account:</strong> 
        <ul>
            <li>Ensures the user is logged out before proceeding.</li>
            <li>Navigates to the login page.</li>
            <li>Logs into the ACME System1 website using the provided email and password.</li>
        </ul>
    </li>
    <li><strong>Get Work Items:</strong> 
        <ul>
            <li>Navigates to the Work Items page within ACME System1.</li>
            <li>Extracts all work items across multiple pages for processing.</li>
        </ul>
    </li>
    <li><strong>Launch ACME System3 Desktop Application:</strong> 
        <ul>
            <li>Opens the ACME System3 desktop application.</li>
            <li>Logs into the application using the provided email and password.</li>
            <li>Navigates to the "Search by ID" window in the desktop application.</li>
        </ul>
    </li>
    <li><strong>Process Each Work Item:</strong> 
        <ul>
            <li>For each work item retrieved from ACME System1:</li>
            <li>Navigates to the specific work item page on the ACME System1 website.</li>
            <li>Extracts key information from the work item: User ID, Account Amount, and Account Number.</li>
        </ul>
    </li>
    <li><strong>Search for Work Item in ACME System3:</strong> 
        <ul>
            <li>In ACME System3, searches for each work item by ID using the "Search by ID" window.</li>
            <li>Opens the client details window.</li>
            <li>Opens the client accounts window.</li>
            <li>Navigates to the account movements window.</li>
            <li>Displays all account movements for the client and extracts the movement details.</li>
        </ul>
    </li>
    <li><strong>Close Unwanted Windows:</strong> 
        <ul>
            <li>Closes all unnecessary windows in ACME System3 and returns to the "Search by ID" window to prepare for the next search.</li>
        </ul>
    </li>
    <li><strong>Update Work Item in ACME System1:</strong> 
        <ul>
            <li>After extracting the necessary information from ACME System3, navigates back to the ACME System1 website.</li>
            <li>Opens the update work item page.</li>
            <li>Sets the comment and updates the status of the work item based on the extracted information.</li>
            <li>Closes the update work item page.</li>
        </ul>
    </li>
    <li><strong>Repeat Process for Remaining Work Items:</strong> 
        <ul>
            <li>The process loops through all remaining work items, repeating steps 5 to 8 for each item.</li>
        </ul>
    </li>
</ol>

</details>

<h2>Conclusion</h2>
<p>This project leverages the power of UiPath automation across both web and desktop platforms to efficiently handle a complex workflow. It automates logging into multiple systems, extracting detailed client data, updating work items, and ensuring that all operations are completed without manual intervention.</p>
<p>By utilizing the three custom libraries for Google Search, ACME System1, and ACME System3, the project achieves a high degree of automation, saving time and reducing the risk of human error.</p>

<h2>Prerequisites</h2>
<ul>
    <li>UiPath Studio (latest version)</li>
    <li>Installed ACME System3 desktop application</li>
    <li>Google Chrome browser</li>
    <li>Valid ACME System1 and ACME System3 account credentials</li>
</ul>
