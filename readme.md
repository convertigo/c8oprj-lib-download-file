


# lib_download_file

Library to trigger a file download from a sequence called with the .bin requester. 


For more technical informations : [documentation](./project.md)

- [Installation](#installation)
- [Sequences](#sequences)
    - [demo_lib_usage](#demo_lib_usage)
    - [get_file](#get_file)
- [Mobile Library](#mobile-library)
    - [Shared Actions](#shared-actions)
        - [getFile](#getfile)


## Installation

1. In your Convertigo Studio click on ![](https://github.com/convertigo/convertigo/blob/develop/eclipse-plugin-studio/icons/studio/project_import.gif?raw=true "Import a project in treeview") to import a project in the treeview
2. In the import wizard

   ![](https://github.com/convertigo/convertigo/blob/develop/eclipse-plugin-studio/tomcat/webapps/convertigo/templates/ftl/project_import_wzd.png?raw=true "Import Project")
   
   paste the text below into the `Project remote URL` field:
   <table>
     <tr><td>Usage</td><td>Click the copy button at the end of the line</td></tr>
     <tr><td>To contribute</td><td>

     ```
     lib_download_file=https://github.com/convertigo/c8oprj-lib-download-file.git:branch=master
     ```
     </td></tr>
     <tr><td>To simply use</td><td>

     ```
     lib_download_file=https://github.com/convertigo/c8oprj-lib-download-file/archive/master.zip
     ```
     </td></tr>
    </table>
3. Click the `Finish` button. This will automatically import the __lib_download_file__ project


## Sequences

### demo_lib_usage

Demo sequence to show the get_file sequence usage

**variables**

<table>
<tr>
<th>name</th><th>comment</th>
</tr>
<tr>
<td>file</td><td>Absolute path to the file to download.<br>
Or use './/' to a file path relative to project folder.<br>
Or use './' to a file path relative to workspace folder.</td>
</tr>
</table>

### get_file

Private sequence to be called from a parent sequence. The parent sequence must be called with .bin requester.

**variables**

<table>
<tr>
<th>name</th><th>comment</th>
</tr>
<tr>
<td>file_path</td><td>Absolute path to the file to download.</td>
</tr>
</table>

## Mobile Library

Describes the mobile application global properties

### Shared Actions

#### getFile

**variables**

<table>
<tr>
<th>name</th><th>comment</th>
</tr>
<tr>
<td>file_path</td><td></td>
</tr>
</table>



