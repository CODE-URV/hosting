# hosting
Repository to store and serve assets.

## About
All files in a GitHub repositories are served statically via `raw.githubusercontent.com`. 

Files can be retrieved using HTTP GET against the corresponding URL endpoint. 

The URL endpoint to retrieve a certain file can be computed using the following:
* The location of the desired file in the repository tree.
* The branch the file is in.
* Repository name.
* Organization.

The URL endpoint to retrieve a certain file can be obtained from GitHub web interface for file that can be viewed as 
raw.

## Usage
### Upload file
Upload the file into the `assets/` folder and push to the repository. Any branch will do. After the push the file is 
served by GitHub. 

### Compute URL
You can either compute it or obtain it directly in the case of files that can be viewed as "raw". Images cannot be 
viewed as raw, they are downloaded directly, but the link that triggers the download is presumably the URL that we want 
to obtain.

###### Compute manually from the URL to the file in GitHub web interface
We need the URL to the file that we want to serve from GitHub web interface. For example, for the file 
`./assets/code-urv-logo.png`, its URL in GitHub web interface is:

[https://github.com/CODE-URV/hosting/blob/master/assets/code-urv-logo.png](https://github.com/CODE-URV/hosting/blob/master/assets/code-urv-logo.png)

We can understand it as:

[https://github.com/ORGANIZATION/REPO/blob/BRANCH/PATH/TO/FILE](https://DOMAIN/ORGANIZATION/REPO/blob/BRANCH/PATH/TO/FILE.png)

To transform that URL into the URL that is statically serving the file we will apply this formula:

[https://raw.githubusercontent.com/ORGANIZATION/REPO/refs/heads/BRANCH/PATH/TO/FILE](https://raw.githubusercontent.com/ORGANIZATION/REPO/refs/heads/BRANCH/PATH/TO/FILE)

So, in the case of [https://github.com/CODE-URV/hosting/blob/master/assets/code-urv-logo.png](https://github.com/CODE-URV/hosting/blob/master/assets/code-urv-logo.png),
its corresponding URL is [https://raw.githubusercontent.com/CODE-URV/hosting/refs/heads/master/assets/code-urv-logo.png](https://raw.githubusercontent.com/CODE-URV/hosting/refs/heads/master/assets/code-urv-logo.png).

###### Obtain from GitHub web interface 
If you enter into a file in GitHub web interface and there is a *raw* button for that file, click it, and copy the URL.

That URL points statically to your desired file. 

### Retrieve / use file
###### curl, wget, etc
```shell
wget https://raw.githubusercontent.com/CODE-URV/hosting/refs/heads/master/assets/code-urv-logo.png
```

```shell
curl https://raw.githubusercontent.com/CODE-URV/hosting/refs/heads/master/assets/code-urv-logo.png
```

###### Markdown 
```markdown
![Logo CODE URV](https://raw.githubusercontent.com/CODE-URV/hosting/refs/heads/master/assets/code-urv-logo.png)
```

With this result:

![Logo CODE URV](https://raw.githubusercontent.com/CODE-URV/hosting/refs/heads/master/assets/code-urv-logo.png)

###### HTML
```html
<img src="https://raw.githubusercontent.com/CODE-URV/hosting/refs/heads/master/assets/code-urv-logo.png" alt="Logo CODE URV"/>
```

With this result (same result as in Markdown section):

<img src="https://raw.githubusercontent.com/CODE-URV/hosting/refs/heads/master/assets/code-urv-logo.png" alt="Logo CODE URV"/>



<!-- CONTRIBUTING -->
## Contributing
This is an open-source project, so any contributions are **greatly appreciated** ❤️. 

If you have an issue or suggestion that would make `hosting` better, please 
[open a new issue](https://github.com/CODE-URV/hosting/issues/new) explaining your inquiry. We will try to satisfy your 
needs as soon as possible. 

If you want to make a contribution to `hosting` by yourself, please 
[open a new issue](https://github.com/CODE-URV/hosting/issues/new), so we can discuss the reach of your contribution. 
After that, [fork the repo](https://github.com/CODE-URV/hosting/fork), implement your change and create a 
[pull request](https://github.com/CODE-URV/hosting/compare) from your fork to the `master` branch. We will merge your 
changes as soon as possible, so they are available in the next releases of `hosting`.

Do not forget to give the project a star ⭐ on GitHub!



<!-- LICENSE -->
## License
![APGLv3 logo](https://www.gnu.org/graphics/agplv3-with-text-162x68.png "GNU AFFERO GENERAL PUBLIC LICENSE, Version 3")

Distributed under the [GNU AFFERO GENERAL PUBLIC LICENSE, Version 3](https://www.gnu.org/licenses/agpl-3.0.en.html). 
See [`LICENSE`](https://github.com/CODE-URV/.github/blob/master/LICENSE) to obtain a copy of the therms of this license.

**`hosting` ultimately belongs to [Aleix Mariné-Tena](https://github.com/AleixMT) and has the control over the licensing
and distribution therms.**

>Copyright 2025 [Aleix Mariné-Tena](https://github.com/AleixMT) 

>This program is free software: you can redistribute it and/or modify it under the terms of the GNU Affero General Public
License as published by the Free Software Foundation, either version 3 of the License, or (at your option) any later 
version.
> 
>This program is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the GNU Affero General Public License for more details.

This software was developed with love ❤️ by [Aleix Mariné-Tena](https://github.com/AleixMT) for CODE URV to store and 
serve its logo and other possible assets. 



## Credits
### Institutions involved in the `hosting` project
![Logo CODE URV](https://raw.githubusercontent.com/CODE-URV/hosting/refs/heads/master/assets/code-urv-logo.png)
- [CODE URV](https://www.github.com/CODE-URV): CODE URV, Association of Computer Scientists at the Rovira i Virgili 
University, mainly composed of students from the ETSE (School of Engineering).


### People involved in the `hosting` development
* **Aleix Mariné-Tena**: Main developer of `hosting`.