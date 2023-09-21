<h1>Command line for the win.</hq>
<hr />
<indent><strong>Language:</strong>Bash</indent>
<hr />
<h3>Objectives met:</h3>
<ul>
<li>Done the CMD ChALLENGE</li>
<li>Taken screenshots as proof.</li>
<li>Used sftp to to move the screenshots to server based virtual machine.</li>
</ul>
<h2>Procedure I used to upload the screenshots to the sandbox.</h2>

1. First, I opened a `SFTP` socket connection with the remote server via the command:
```
sftp <user>@<hostname>
```

2. Then, I input the password as requested by the interactive `SFTP` shell.

3. I followed this step by switching to the desired remote directory:
```
sftp> cd desired_directory
```

4. Then I switched my local directory to the appropriate one:
```
sftp> lcd appropriate_dir
```

5. Next, I transfered the directory containing the screen shots to the server:
```
sftp> put -r screen_shot_dir
```

6. Finally, I checked for the success by listing the contents of the remote working directory.
```
sftp> ls
```

7. This confirmed my success and so I exited the `SFTP` interactive shell:
```
sftp> exit
```
