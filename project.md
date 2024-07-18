
# ![](https://github.com/convertigo/convertigo/blob/develop/engine/src/com/twinsoft/convertigo/beans/core/images/project_color_16x16.png?raw=true "Project") lib_download_file

This library will enable your applications to download files held on Convertigo server.

## Purpose
In many applications, it is useful to provide buttons or links to trigger a file download of a file (PDF, Document, Photo etc ... ) generated or held on a file system accessible by a Convertigo server. By default, Convertigo can only serve files located in the project workspace, without controlling access to these file. If you want to serve files located outside the workspace and want a fined grained control with some business logic to enable or not the download, you should use this library.

## Usage
The back-end part of the library is the **get_file** sequence. This is a **private** sequence so it cannot be called directly by a client. You must create your own sequence controlling the business logic and if the user is enabled to do so call the **get_file** sequence within you own custom sequence.

The library provides a sample **demo_lib_usage** showing this

On the Front-end side, you must trigger a file download by calling this custom sequence. To do so the library  provides a **getFile** SharedAction you can use within your project. A Sample application with a "Download File" button is provided showing how to call this Shared Action from your project.



<details><summary><span style="color:DarkGoldenRod"><i>Connectors</i></span></summary><blockquote><p>


## ![](https://github.com/convertigo/convertigo/blob/develop/engine/src/com/twinsoft/convertigo/beans/connectors/images/sqlconnector_color_16x16.png?raw=true "SqlConnector") void

void connector, replace or don't use it

<details><summary><span style="color:DarkGoldenRod"><i>Transactions</i></span></summary><blockquote><p>


### ![](https://github.com/convertigo/convertigo/blob/develop/engine/src/com/twinsoft/convertigo/beans/transactions/images/sqltransaction_color_16x16.png?raw=true "SqlTransaction") void

does nothing
</p></blockquote></details>
</p></blockquote></details>

<details><summary><span style="color:DarkGoldenRod"><i>Sequences</i></span></summary><blockquote><p>


<details><summary><b>demo_lib_usage</b> : Demo sequence to show the get_file sequence usage</summary><blockquote><p>


## ![](https://github.com/convertigo/convertigo/blob/develop/engine/src/com/twinsoft/convertigo/beans/sequences/images/genericsequence_color_16x16.png?raw=true "GenericSequence") demo_lib_usage

Demo sequence to show the get_file sequence usage

<span style="color:DarkGoldenRod">Variables</span>

<table>
<tr>
<th>
name
</th>
<th>
comment
</th>
</tr>
<tr>
<td>
<img src="https://github.com/convertigo/convertigo/blob/develop/engine/src/com/twinsoft/convertigo/beans/variables/images/variable_color_16x16.png?raw=true "  alt="RequestableVariable" >&nbsp;file_path
</td>
<td>
Absolute path to the file to download.<br>
Or use './/' to a file path relative to project folder.<br>
Or use './' to a file path relative to workspace folder.
</td>
</tr>
</table>

</p></blockquote></details>

<details><summary><b>get_file</b> : Private sequence to be called from a parent sequence</summary><blockquote><p>


## ![](https://github.com/convertigo/convertigo/blob/develop/engine/src/com/twinsoft/convertigo/beans/sequences/images/genericsequence_color_16x16.png?raw=true "GenericSequence") get_file

Private sequence to be called from a parent sequence. The parent sequence must be called with .bin requester.

<span style="color:DarkGoldenRod">Variables</span>

<table>
<tr>
<th>
name
</th>
<th>
comment
</th>
</tr>
<tr>
<td>
<img src="https://github.com/convertigo/convertigo/blob/develop/engine/src/com/twinsoft/convertigo/beans/variables/images/variable_color_16x16.png?raw=true "  alt="RequestableVariable" >&nbsp;file_path
</td>
<td>
Absolute path to the file to download.
</td>
</tr>
</table>

</p></blockquote></details>
</p></blockquote></details>

<details><summary><span style="color:DarkGoldenRod"><i>Mobile Application</i></span></summary><blockquote><p>


## ![](https://github.com/convertigo/convertigo/blob/develop/engine/src/com/twinsoft/convertigo/beans/core/images/mobileapplication_color_16x16.png?raw=true "MobileApplication") Application

The shared action <b>getFile</b> is used to trigger a download file in a Convertigo NGX Application.<br>
Drag and Drop the <b>getFile</b> shared action in an event (onClick of a button, for example) and set the <b>file _path</b> variable to the path of the file to download from Convertigo Server filesystem and the <b>target_sequence</b> variable to your main sequence.

<details><summary><span style="color:DarkGoldenRod"><i>Pages</i></span></summary><blockquote><p>


### ![](https://github.com/convertigo/convertigo/blob/develop/engine/src/com/twinsoft/convertigo/beans/ngx/components/images/pagecomponent_color_16x16.png?raw=true "PageComponent") Page


</p></blockquote></details>

<details><summary><span style="color:DarkGoldenRod"><i>Shared Actions</i></span></summary><blockquote><p>


### ![](https://github.com/convertigo/convertigo/blob/develop/engine/src/com/twinsoft/convertigo/beans/ngx/components/images/uiactionstack_color_16x16.png?raw=true "UIActionStack") getFile

Action to trigger a file download in your Application.

<span style="color:DarkGoldenRod">Variables</span>

<table>
<tr>
<th>
name
</th>
<th>
comment
</th>
</tr>
<tr>
<td>
<img src="https://github.com/convertigo/convertigo/blob/develop/engine/src/com/twinsoft/convertigo/beans/ngx/components/images/uistackvariable_16x16.png?raw=true "  alt="UIStackVariable" >&nbsp;callback
</td>
<td>
Callback sequence. This is the parent sequence performing the control business logic that finally calls the get_file sequence to perform the file download.
</td>
</tr>
<tr>
<td>
<img src="https://github.com/convertigo/convertigo/blob/develop/engine/src/com/twinsoft/convertigo/beans/ngx/components/images/uistackvariable_16x16.png?raw=true "  alt="UIStackVariable" >&nbsp;file
</td>
<td>
The path to a file on the server to download. The path can be absolute , relative to the project (.//) or relative to the workspace (./) 
</td>
</tr>
</table>

</p></blockquote></details>
</p></blockquote></details>
