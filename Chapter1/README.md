# Chapter 1: What is Version Control?

## Tracking File History

Version Control Software (VCS) helps users track the history of a file or group of files in an organized manner. The basic tenet is that previous versions can be retrieved at any time. There are many different ways to accomplish version control including: scheduled automatic backups, basic manual backups, and annotated manual backups, each with their own benefits and drawbacks. Some examples you may recognize include the history functionality on Google Docs and Apple's Time Machine service.

Many people use version control software to backup their files to the cloud or to an external hard drive. This is normally to preserve their files so that in the case of a computer issue, their files will still exist on a secondary storage device. Apple's Time Machine is an example of such a system, which creates backups of files at scheduled intervals. This automatic backup style allows users to forget about it until they need to retrieve a file.

<svg width="600" height="400">
  <style>
    #file_icon {
      animation: slide_down 5s infinite;
    }
    @keyframes slide_down {
      0% {
        transform: translate(0, 0);
      }
      20% {
        transform: translate(0, 50px);
      }
      100% {
        transform: translate(0, 50px);
      }
    }

    #clock_hand {
      transform-origin: bottom right;
      transform-box: fill-box;
      animation: spin 5s linear infinite;
    }
    @keyframes spin {
      100% { transform: rotate(360deg); }
    }
  </style>
  <svg class="svg-icon" viewBox="10 -5 100 100" id="file_icon_svg">
    <path d="M15.475,6.692l-4.084-4.083C11.32,2.538,11.223,2.5,11.125,2.5h-6c-0.413,0-0.75,0.337-0.75,0.75v13.5c0,0.412,0.337,0.75,0.75,0.75h9.75c0.412,0,0.75-0.338,0.75-0.75V6.94C15.609,6.839,15.554,6.771,15.475,6.692 M11.5,3.779l2.843,2.846H11.5V3.779z M14.875,16.75h-9.75V3.25h5.625V7c0,0.206,0.168,0.375,0.375,0.375h3.75V16.75z" id="file_icon">
    </path>
  </svg>
  <circle cx="300" cy="50" r="30" stroke="black" stroke-width="3" fill="None"> </circle>
  <line x1="300" y1="50" x2="300" y2="20" stroke="black" id="clock_hand"> </line>
  <line x1="300" y1="15" x2="300" y2="10" stroke="black"> </line>
</svg>

Automatic version control either backs up files at set intervals or detects when changes are saved and backs up at that time. The user does not need to do anything for these backups to be created, but since they do not have any input on the backed up content, there's no guarantee that every backup will be at a useful point in the history of the file; it may be between logical revisions or in the middle of a change. Automated backup systems generally require a lot of storage space due to the extraneous backup copies.

Manual version control cedes much more control to the user, along with the responsibility of generating more meaningful revisions to save. One basic example of a fully manual version control system is manually saving copies of files to preserve each version. This is generally not advised since it can clutter up folders and usually ends up disorganized. Some applications handle this for you: Sharepoint for example allows users to "check out" files like library books, edit them, and check them back in when they're done with the file.

The type of version control we will be learning about in this course is a specific application that allows users to backup their work whenever they want, but it enforces some better record keeping by requiring users to annotate all backups. The most common VCS of this type is called Git, which we will be learning about.

Git is a VCS developed primarily for use by software developers. Git shines when the files being tracked are primarily plain-text files, like code or raw data, but it can also be used for any type of file. Git finds efficiency by only storing changes from one backup, called a "commit," to the next. In addition to the changes, each commit stores the author, date and time, and a message that the user must fill about about what changes were made. The verbosity of this message is up to the individual user, so its usefulness is determined by the user's upfront effort.

## Collaboration

Another important feature of most VCS systems is the ability to share files and collaborate with others. The VCS style used and the way the system is set up greatly impacts the ease of collaboration. 
