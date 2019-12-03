This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app).

## Simple Bash Scripts ######################### 
## FileName: mkreact.sh
#!/bin/sh

if [ ! -d "$HOME"/git-sources ]; then
    mkdir "$HOME"/git-sources
fi
printf "AppName: "
read -r AppName 

gitsource="https://github.com/king0fCode/basic-react-template.git"
git clone "$gitsource"  "$AppName"
unset gitsource

AppDir="$(pwd)/$AppName"
echo "App Created  in $AppDir"
cd "$AppDir" && npm i -y
echo "App Dependencies Installed"

echo "Please choose from the options bellow"
echo "1) Open App directory"
echo "2) Open App with Visual Studio Code"
echo "3) Exit"

read -r ans
directory="1"
code="2"
end="3"

if [ "$ans" = "$directory" ]; then
xdg-open .
unset ans; 
return 1;

elif [ "$ans" = "$code" ]; then
code .
return 1;

elif [ "$ans" = "$end" ]; then
exit
fi

unset ans


############################################

### `add mkreact.sh bash to linux path`
### `type this on console`

chmod u+x,g+x mkreact.sh && echo " alias mkreact='/home/drcode/mkreact.sh'" >> .bashrc && source ~/.bashrc

### now you can run it anywhere to create react basic app.. in terminal type `mkreact` command to begin 
##############################################


### `npm test`

Launches the test runner in the interactive watch mode.<br />
See the section about [running tests](https://facebook.github.io/create-react-app/docs/running-tests) for more information.

### `npm run build`

Builds the app for production to the `build` folder.<br />
It correctly bundles React in production mode and optimizes the build for the best performance.

The build is minified and the filenames include the hashes.<br />
Your app is ready to be deployed!

See the section about [deployment](https://facebook.github.io/create-react-app/docs/deployment) for more information.

### `npm run eject`

**Note: this is a one-way operation. Once you `eject`, you can’t go back!**

If you aren’t satisfied with the build tool and configuration choices, you can `eject` at any time. This command will remove the single build dependency from your project.

Instead, it will copy all the configuration files and the transitive dependencies (Webpack, Babel, ESLint, etc) right into your project so you have full control over them. All of the commands except `eject` will still work, but they will point to the copied scripts so you can tweak them. At this point you’re on your own.

You don’t have to ever use `eject`. The curated feature set is suitable for small and middle deployments, and you shouldn’t feel obligated to use this feature. However we understand that this tool wouldn’t be useful if you couldn’t customize it when you are ready for it.

## Learn More

You can learn more in the [Create React App documentation](https://facebook.github.io/create-react-app/docs/getting-started).

To learn React, check out the [React documentation](https://reactjs.org/).

### Code Splitting

This section has moved here: https://facebook.github.io/create-react-app/docs/code-splitting

### Analyzing the Bundle Size

This section has moved here: https://facebook.github.io/create-react-app/docs/analyzing-the-bundle-size

### Making a Progressive Web App

This section has moved here: https://facebook.github.io/create-react-app/docs/making-a-progressive-web-app

### Advanced Configuration

This section has moved here: https://facebook.github.io/create-react-app/docs/advanced-configuration

### Deployment

This section has moved here: https://facebook.github.io/create-react-app/docs/deployment

### `npm run build` fails to minify

This section has moved here: https://facebook.github.io/create-react-app/docs/troubleshooting#npm-run-build-fails-to-minify
