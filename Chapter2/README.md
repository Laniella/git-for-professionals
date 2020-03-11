# Chapter 2: Why Use Version Control?

As discussed in Chapter 1, there are many ways to accomplish version control, some better suited to different use cases than others. In this chapter, we'll explore the reasons why using a dedicated version control system is, in many cases, the best option.

## Options for Version Control

There are many ways to do version control, all of which can be scored on a few different attributes. We'll be looking at these options with regards to how easy it is to perform some different tasks generally associated with version control systems. Note that some of these options are not dedicated software and require more manual effort than others. Let's begin by looking at a table to summarize some high level differences between the version control approaches.

|Version control approach|Saving new versions|Retrieving desired old version|Sharing|Collaboration|
|------------------------|-------------------|------------------------------|-------|-------------|
|File Copies             |Easy|Very Hard|Moderate|Very Hard|
|Automated Backup        |Very Easy|Moderate|Hard|Very Hard|
|Cloud Storage           |Easy|Moderate|Easy|Moderate|
|Dedicated VCS           |Moderate|Very Easy|Easy|Very Easy|

### Saving New Versions

This is the most basic feature a version control system must have. The ability to save new versions of files is basic, but has nuances in how it is handled. Select each tab below to learn about how the approaches above differ.

<div class="interactive_area">
  <!-- Tab links -->
  <div class="tab">
    <button class="tablinks" onclick="openTab(event, 'file_copies_1')">File Copies</button>
    <button class="tablinks" onclick="openTab(event, 'automated_backup_1')">Automated Backup</button>
    <button class="tablinks" onclick="openTab(event, 'cloud_storage_1')">Cloud Storage</button>
    <button class="tablinks" onclick="openTab(event, 'dedicated_vcs_1')">Dedicated VCS</button>
  </div>
  
  <!-- Tab content -->
  <div id="file_copies_1" class="tabcontent">
    <h3>Manually Saving File Copies</h3>
    <p>Saving new versions with this method simply involves performing a "Save As" action from whatever application the file is being edited in. This does require the user to select a new name that hasn't been used before.</p>
    <p>A common convention is appending the date and time to the file when saving. This is a straightforward task that most users would be comfortable doing.</p>
  </div>
  
  <div id="automated_backup_1" class="tabcontent">
    <h3>Automated Backup (Time Machine)</h3>
    <p>No user action is required here to save new versions. The automated backup will run on its own. Once set up, this requires no effort from the user.</p>
  </div>
  
  <div id="cloud_storage_1" class="tabcontent">
    <h3>Cloud Storage (Sharepoint/Google Drive)</h3>
    <p>There is some variance in interface between specific cloud storage solutions here, but in general, users need to upload files they want to save whenever they want a revision saved.</p>
    <p>This is a straightforward action, although does include an extra step beyond just saving a file locally.</p>
  </div>

  <div id="dedicated_vcs_1" class="tabcontent">
    <h3>Dedicated VCS (Git)</h3>
    <p>This approach requires comparatively the most effort. Users need to select the specific changes they want to back up and then add a note about what changed. While this can be more work, users will often just add all changes they have made, eliminating the need to select specific changes.</p>
    <p>As we will see next, although writing a note about what has been changed requires more upfront effort when saving, the notes become very helpful for other version control tasks.</p>
  </div>
</div>

### Retrieving Old Versions

After having collected a backlog of versions, users should be able to go back to an older version on demand. Explore below how each approach handles the retrieval of old versions of files.

<div class="interactive_area">
  <!-- Tab links -->
  <div class="tab">
    <button class="tablinks" onclick="openTab(event, 'file_copies_2')">File Copies</button>
    <button class="tablinks" onclick="openTab(event, 'automated_backup_2')">Automated Backup</button>
    <button class="tablinks" onclick="openTab(event, 'cloud_storage_2')">Cloud Storage</button>
    <button class="tablinks" onclick="openTab(event, 'dedicated_vcs_2')">Dedicated VCS</button>
  </div>
  
  <!-- Tab content -->
  <div id="file_copies_2" class="tabcontent">
    <h3>Manually Saving File Copies</h3>
    <p>In this case, users normally have lots of files with similar names in a folder. It's often quite difficult to know what each version contains since the only information is the file name.</p>
    <p>With no information about what each copy contains or when each copy was saved, it's very difficult to locate a specific version when trying.</p>
  </div>
  
  <div id="automated_backup_2" class="tabcontent">
    <h3>Automated Backup (Time Machine)</h3>
    <p>Automated backups make it easy to find a version of a file based on time, but they generally do not contain much information about what was changed. Since files are backed up at regular intervals, it's unlikely work will be lost, but if a user needs something from more than a few hours or days previous, it can take more effort to find the correct version.</p>
  </div>
  
  <div id="cloud_storage_2" class="tabcontent">
    <h3>Cloud Storage (Sharepoint/Google Drive)</h3>
    <p>Cloud storage has similar properties to automated backups. There's usually not much information about what was changed, but since every save is uploaded manually, there's a good chance that each entry in the file history is useful.</p>
    <p>In this case, it's still moderately difficult to locate a specific version of a file.</p>
  </div>

  <div id="dedicated_vcs_2" class="tabcontent">
    <h3>Dedicated VCS (Git)</h3>
    <p>Dedicated VCS like Git enforces a change message with every change, so looking back through the history, it's relatively easy to see what was done at each point. For some file types, version control systems will easily show the state of the file and the changes made from there at any point in the history.</p>
    <p>This ability to quickly determine what changed at each point in the file history makes it very simple to locate any specific version of a file. Furthermore, the VCS will track all files simultaneously, so it's possible to see the states of multiple files at any point in the past, ensuring that they match up.</p>
  </div>
</div>

### Sharing

The ability to share files with other users can be very useful as well. Some version control systems provide an easy mechanism for sharing files.

<div class="interactive_area">
  <!-- Tab links -->
  <div class="tab">
    <button class="tablinks" onclick="openTab(event, 'file_copies_3')">File Copies</button>
    <button class="tablinks" onclick="openTab(event, 'automated_backup_3')">Automated Backup</button>
    <button class="tablinks" onclick="openTab(event, 'cloud_storage_3')">Cloud Storage</button>
    <button class="tablinks" onclick="openTab(event, 'dedicated_vcs_3')">Dedicated VCS</button>
  </div>
  
  <!-- Tab content -->
  <div id="file_copies_3" class="tabcontent">
    <h3>Manually Saving File Copies</h3>
    <p>Sharing files as they exist on your computer is as easy or hard as sending them via email or some other file exchange application. Nothing about this process is automated though, so users must manually select and send the files they want.</p>
  </div>
  
  <div id="automated_backup_3" class="tabcontent">
    <h3>Automated Backup (Time Machine)</h3>
    <p>Most backup systems are not intended for sharing with others. Backups are stored away on a hard drive and usually hidden behind the automated backup application. Sending a file from here usually requires downloading or reverting to the desired version before sending with email or some other file exchange application. Not a very simple process.</p>
  </div>
  
  <div id="cloud_storage_3" class="tabcontent">
    <h3>Cloud Storage (Sharepoint/Google Drive)</h3>
    <p>Sharing files from cloud storage is very straightforward since they normally have a built in share feature. Users can get links to files and easily share them.</p>
    <p>One caveat here is that to share an older version, it's still usually required to revert the file to the desired version before sharing.</p>
  </div>

  <div id="dedicated_vcs_3" class="tabcontent">
    <h3>Dedicated VCS (Git)</h3>
    <p>Git and other version control systems have the concept of collaboration built in, so multiple users can have copies of the tracked files on their computers. Since it's all centrally managed, users will have access to the same logged file history, so sharing a file is as easy as sending the specific code for a point in history. Since old versions are tracked with codes, users are able to share older versions without modifying their local copy.</p>
  </div>
</div>

### Collaboration

It's often even more useful to work together with others simultaneously on the same file or files. Some version control systems help manage collaboration by tracking each user's changes.

<div class="interactive_area">
  <!-- Tab links -->
  <div class="tab">
    <button class="tablinks" onclick="openTab(event, 'file_copies_4')">File Copies</button>
    <button class="tablinks" onclick="openTab(event, 'automated_backup_4')">Automated Backup</button>
    <button class="tablinks" onclick="openTab(event, 'cloud_storage_4')">Cloud Storage</button>
    <button class="tablinks" onclick="openTab(event, 'dedicated_vcs_4')">Dedicated VCS</button>
  </div>
  
  <!-- Tab content -->
  <div id="file_copies_4" class="tabcontent">
    <h3>Manually Saving File Copies</h3>
    <p>There is no management for collaboration with this approach. It's very difficult to maintain a file that has multiple people contributing to it.</p>
  </div>
  
  <div id="automated_backup_4" class="tabcontent">
    <h3>Automated Backup (Time Machine)</h3>
    <p>There is no management for collaboration with this approach. It's very difficult to maintain a file that has multiple people contributing to it.</p>
  </div>
  
  <div id="cloud_storage_4" class="tabcontent">
    <h3>Cloud Storage (Sharepoint/Google Drive)</h3>
    <p>This approach incorporates some collaboration features, depending on which cloud storage solution is used.</p>
    <p>Sharepoint, for instance, allows users to "check out" and lock a file so that no other users can edit it until it has been checked back in. This ensures there will not be any conflicts from two users changing the same file simultaneously, but also prevents some cases where multiple people may want to contribute together. Users also need to remember to check files back in after editing them.</p>
    <p>Google Drive allows real time collaboration for their exclusive file types, but does not prevent overwriting another user's edits for files that are simply tracked.</p>
  </div>

  <div id="dedicated_vcs_4" class="tabcontent">
    <h3>Dedicated VCS (Git)</h3>
    <p>Git and other version control systems are extremely powerful for allowing multiple users to contribute simultaneously. Since versions are stored by the VCS as changes from the previous version of the file, there is a function called merging that allows multiple changes to the same baseline to be applied together, provided that they do not directly conflict. Even if there is a conflict between two changes, the tool allows users to manually arbitrate what changes go in.</p>
  </div>
</div>

## [Chapters 1 and 2 Review](https://docs.google.com/forms/d/e/1FAIpQLSfR8U1BG0grUf7HWuGJ9AoIWojtY48rpNyKCR5G2mg4q6gHRg/viewform?usp=sf_link)

Please go through this quick review before continuing on to Chapter 3.

### [Chapter 3: Introduction to Git](../Chapter3)

<style>
/* Style the tab */
.tab {
  overflow: hidden;
  border: 1px solid #333;
  background-color: #333;
}

/* Style the buttons that are used to open the tab content */
.tab button {
  background-color: inherit;
  float: left;
  border: none;
  outline: none;
  cursor: pointer;
  padding: 14px 16px;
  transition: 0.3s;
  color: #cfcfcf;
}

/* Change background color of buttons on hover */
.tab button:hover {
  background-color: #777;
}

/* Create an active/current tablink class */
.tab button.active {
  background-color: #555;
}

/* Style the tab content */
.tabcontent {
  display: none;
  padding: 6px 20px;
  border: 1px solid #333;
  border-top: none;
}
</style>
<script type="text/javascript">
function openTab(evt, tabName) {
  // Declare all variables
  var i, tabcontent, tablinks;

  // Get all elements with class="tabcontent" and hide them
  tabcontent = document.getElementsByClassName("tabcontent");
  for (i = 0; i < tabcontent.length; i++) {
    tabcontent[i].style.display = "none";
  }

  // Get all elements with class="tablinks" and remove the class "active"
  tablinks = document.getElementsByClassName("tablinks");
  for (i = 0; i < tablinks.length; i++) {
    tablinks[i].className = tablinks[i].className.replace(" active", "");
  }

  // Show the current tab, and add an "active" class to the button that opened the tab
  document.getElementById(tabName).style.display = "block";
  evt.currentTarget.className += " active";
}
function colorCells() {
  var cells = document.getElementsByTagName("td");

  for(var idx = 0; idx < cells.length; ++idx) {
    switch(cells[idx].innerText) {
      case "Very Easy":
        cells[idx].style.backgroundColor = "#34FD9A";
        break;
      case "Easy":
        cells[idx].style.backgroundColor = "#79D0AC";
        break;
      case "Moderate":
        cells[idx].style.backgroundColor = "#ECEBBB";
        break;
      case "Hard":
        cells[idx].style.backgroundColor = "#F2C1A3";
        break;
      case "Very Hard":
        cells[idx].style.backgroundColor = "#F9BCA1";
        break;
    }
  }
}
openTab(event, 'file_copies_1')
colorCells()
</script>

