


# lib_download_file

This library will enable your applications to download files held on Convertigo server.

## Purpose
In many applications, it is useful to provide buttons or links to trigger a file download of a file (PDF, Document, Photo etc ... ) generated or held on a file system accessible by a Convertigo server. By default, Convertigo can only serve files located in the project workspace, without controlling access to these file. If you want to serve files located outside the workspace and want a fined grained control wil some business logic to enable or not the download, you should use this library.

## Usage
The back-end part of the library is the **get_file** sequence. This is a **private** sequence so it cannot be called directly by a client. You must create your own sequence controlling the business logic and if the user is enabled to do so call the **get_file** sequence within you own custom sequence.

The library provides a sample **demo_lib_usage** showing this

On the Front-end side, you must trigger a file download by calling this custom sequence. To do so the library  provides a **getFile** SharedAction you can use within your project. A Sample application with a "Download File" button is provided showing how to call this Shared Action from your project.




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
<td>file_path</td><td>Absolute path to the file to download.<br>
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

The shared action <b>getFile</b> is used to trigger a download file in a Convertigo NGX Application.<br>
Drag and Drop the <b>getFile</b> shared action in an event (onClick of a button, for example) and set the <b>file _path</b> variable to the path of the file to download from Convertigo Server filesystem and the <b>target_sequence</b> variable to your main sequence.

### Shared Actions

#### getFile

Action to trigger a file download in your Application.

**variables**

<table>
<tr>
<th>name</th><th>comment</th>
</tr>
<tr>
<td>callback</td><td>Callback sequence. This is the parent sequence performing the control business logic that finally calls the get_file sequence to perform the file download.</td>
</tr>
<tr>
<td>file</td><td>The path to a file on the server to download. The path can be absolute , relative to the project (.//) or relative to the workspace (./) </td>
</tr>
</table>



