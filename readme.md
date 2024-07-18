


# lib_download_file

Library to trigger a file download from a sequence called with the .bin requester.


For more technical informations : [documentation](./project.md)

- [Installation](#installation)
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
     lib_download_file=C:/Convertigo/Studio 8.2.3/workspace/lib_download_file/.git:branch=master
     ```
     </td></tr>
     <tr><td>To simply use</td><td>

     ```
     lib_download_file=C:/Convertigo/Studio 8.2.3/workspace/lib_download_file//archive/master.zip
     ```
     </td></tr>
    </table>
3. Click the `Finish` button. This will automatically import the __lib_download_file__ project


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



