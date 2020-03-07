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
    <button class="tablinks" onclick="openTab(event, 'file_copies')">File Copies</button>
    <button class="tablinks" onclick="openTab(event, 'automated_backup')">Automated Backup</button>
    <button class="tablinks" onclick="openTab(event, 'cloud_storage')">Cloud Storage</button>
    <button class="tablinks" onclick="openTab(event, 'dedicated_vcs')">Dedicated VCS</button>
  </div>
  
  <!-- Tab content -->
  <div id="file_copies" class="tabcontent">
    <h3>Manually Saving File Copies</h3>
    <p>Saving new versions with this method simply involves performing a "Save As" action from whatever application the file is being edited in. This does require the user to select a new name that hasn't been used before.</p>
    <p>A common convention is appending the date and time to the file when saving. This is a straightforward task that most users would be comfortable doing.</p>
  </div>
  
  <div id="automated_backup" class="tabcontent">
    <h3>Automated Backup (Time Machine)</h3>
    <p>No user action is required here to save new versions. The automated backup will run on its own. Once set up, this requires no effort from the user.</p>
  </div>
  
  <div id="cloud_storage" class="tabcontent">
    <h3>Cloud Storage (Sharepoint/Google Drive)</h3>
    <p>There is some variance in interface between specific cloud storage solutions here, but in general, users need to upload files they want to save whenever they want a revision saved.</p>
    <p>This is a straightforward action, although does include an extra step beyond just saving a file locally.</p>
  </div>

  <div id="dedicated_vcs" class="tabcontent">
    <h3>Dedicated VCS (Git)</h3>
    <p>This approach requires comparatively the most effort. Users need to select the specific changes they want to back up and then add a note about what changed. While this can be more work, users will often just add all changes they have made, eliminating the need to select specific changes.</p>
    <p>As we will see next, although writing a note about what has been changed requires more upfront effort when saving, the notes become very helpful for other version control tasks.
  </div>
</div>
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
  background-color: #ddd;
}

/* Create an active/current tablink class */
.tab button.active {
  background-color: #555;
}

/* Style the tab content */
.tabcontent {
  display: none;
  padding: 6px 12px;
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
</script>

### Retrieving Old Versions

After having collected a backlog of versions, users should be able to go back to an older version on demand. Explore below how each approach handles the retrieval of old versions of files.

<div class="interactive_area">
  <!-- Tab links -->
  <div class="tab">
    <button class="tablinks" onclick="openTab(event, 'file_copies')">File Copies</button>
    <button class="tablinks" onclick="openTab(event, 'automated_backup')">Automated Backup</button>
    <button class="tablinks" onclick="openTab(event, 'cloud_storage')">Cloud Storage</button>
    <button class="tablinks" onclick="openTab(event, 'dedicated_vcs')">Dedicated VCS</button>
  </div>
  
  <!-- Tab content -->
  <div id="file_copies" class="tabcontent">
    <h3>Manually Saving File Copies</h3>
    <p>test1.</p>
  </div>
  
  <div id="automated_backup" class="tabcontent">
    <h3>Automated Backup (Time Machine)</h3>
    <p>test2.</p>
  </div>
  
  <div id="cloud_storage" class="tabcontent">
    <h3>Cloud Storage (Sharepoint/Google Drive)</h3>
    <p>test3.</p>
  </div>

  <div id="dedicated_vcs" class="tabcontent">
    <h3>Dedicated VCS (Git)</h3>
    <p>test4.</p>
  </div>
</div>
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
  background-color: #ddd;
}

/* Create an active/current tablink class */
.tab button.active {
  background-color: #555;
}

/* Style the tab content */
.tabcontent {
  display: none;
  padding: 6px 12px;
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
</script>

### Sharing

The ability to share files with other users can be very useful as well. Some version control systems provide an easy mechanism for sharing files.

// explory thing here where users can select each vcs type and see info

### Collaboration

It's often even more useful to work together with others on the same file or files. Some version control systems help manage collaboration by tracking each user's changes.

// explory thing here where users can select each vcs type and see info

## [Chapters 1 and 2 Review]()

Please go through this quick review before continuing on to Chapter 3.

## [Chapter 3: Introduction to Git](../Chapter3)

