

After cloning the keychron repo 

And installing QMK as per https://docs.qmk.fm/#/newbs_getting_started

    python3 -m pip install --user qmk

    qmk setup

To get repo:

	qmk setup -b bluetooth_playground noodle456/qmk_firmware_keychron

Or just (better)

	git clone --branch bluetooth_playground https://github.com/noodle456/qmk_firmware_keychron.git


Make any changes then in the main folder

Make and flash as per instructions here:
https://github.com/noodle456/qmk_firmware_keychron/tree/bluetooth_playground/keyboards/keychron/k15_pro

	make keychron/k15_pro/ansi_encoder/rgb:default

Where default is the name of the keymap

And to flash - turn keyboard off then plug in USB and switch to cable while holding esc down (to put in bootloader mode)

	make keychron/k15_pro/ansi_encoder/rgb:default:flash


Pushing changes back up from local:
https://docs.qmk.fm/#/getting_started_github

Need to log in use a 'personal access token' in - [Settings](https://github.com/settings/profile)/
- [Developer Settings](https://github.com/settings/apps)]

Use this instead of a password to log in

- [Stage and commit all changes](https://docs.gitlab.com/ee/gitlab-basics/start-using-git.html#stage-and-commit-all-changes)

	git add <file-name OR folder-name>
	git status
	git commit -m "COMMENT TO DESCRIBE THE INTENTION OF THE COMMIT"


As a shortcut, you can add all local changes to staging and commit them with one command:
 
	git commit -a -m "COMMENT TO DESCRIBE THE INTENTION OF THE COMMIT"

Send changes to GitLab.com](https://docs.gitlab.com/ee/gitlab-basics/start-using-git.html#send-changes-to-gitlabcom)

To push all local changes to the remote repository:
    
    
    git push <remote> <name-of-branch>
    

For example, to push your local commits to the `main` branch of the `origin` remote:
    
    
    git push origin main
