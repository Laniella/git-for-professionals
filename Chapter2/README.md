# Chapter 2: Why Use Version Control?

As discussed in Chapter 1, there are many ways to accomplish version control, some better suited to different use cases than others. In this chapter, we'll explore the reasons why using a dedicated version control system is, in many cases, the best option.

## Options for Version Control

There are many ways to do version control, all of which can be scored on a few different attributes. We'll be looking at these options with regards to how easy it is to perform some different tasks generally associated with version control systems. Note that some of these options are not dedicated software and require more manual effort than others. Let's begin by looking at a table to summarize some high level differences between the version control approaches.

|Version control approach|Saving new versions|Retrieving desired old version|Sharing|Collaboration|
|---|-------------------|------------------------------|-------|-------------|
|Storing multiple copies of files|Easy|Very Hard|Moderate|Very Hard|
|Time Machine style backups      |Very Easy|Moderate|Hard|Very Hard|
|Sharepoint/Google Drive         |Easy|Moderate|Easy|Moderate|
|Dedicated VCS (Git)             |Moderate|Very Easy|Easy|Very Easy|

### Saving New Versions

This is the most basic feature a version control system must have. The ability to save new versions of files is basic, but has nuances in how it is handled. 

<div class="interactive_area">
  <!-- Tab links -->
  <div class="tab">
    <button class="tablinks" onclick="openCity(event, 'London')">London</button>
    <button class="tablinks" onclick="openCity(event, 'Paris')">Paris</button>
    <button class="tablinks" onclick="openCity(event, 'Tokyo')">Tokyo</button>
  </div>
  
  <!-- Tab content -->
  <div id="London" class="tabcontent">
    <h3>London</h3>
    <p>London is the capital city of England.</p>
  </div>
  
  <div id="Paris" class="tabcontent">
    <h3>Paris</h3>
    <p>Paris is the capital of France.</p>
  </div>
  
  <div id="Tokyo" class="tabcontent">
    <h3>Tokyo</h3>
    <p>Tokyo is the capital of Japan.</p>
  </div>
</div>
<style>
/* Style the tab */
.tab {
  overflow: hidden;
  border: 1px solid #ccc;
  background-color: #f1f1f1;
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
}

/* Change background color of buttons on hover */
.tab button:hover {
  background-color: #ddd;
}

/* Create an active/current tablink class */
.tab button.active {
  background-color: #ccc;
}

/* Style the tab content */
.tabcontent {
  display: none;
  padding: 6px 12px;
  border: 1px solid #ccc;
  border-top: none;
}
</style>
<script type="text/javascript">
function openCity(evt, cityName) {
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
  document.getElementById(cityName).style.display = "block";
  evt.currentTarget.className += " active";
}
</script>

### Retrieving Old Versions

After having collected a backlog of versions, users should be able to go back to an older version on demand. Explore below how each approach handles the retrieval of old versions of files.

// explory thing here where users can select each vcs type and see info

### Sharing

The ability to share files with other users can be very useful as well. Some version control systems provide an easy mechanism for sharing files.

// explory thing here where users can select each vcs type and see info

### Collaboration

It's often even more useful to work together with others on the same file or files. Some version control systems help manage collaboration by tracking each user's changes.

// explory thing here where users can select each vcs type and see info

## [Chapters 1 and 2 Review]()

Please go through this quick review before continuing on to Chapter 3.

## [Chapter 3: Introduction to Git](Chapter3)

