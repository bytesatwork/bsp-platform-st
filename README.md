# bytes at work AG BSP platform manifest for STM32MP1 based modules

This contains the manifest for [repo](https://source.android.com/setup/develop/repo) and is intended to
simplify the build procedure for byteDEVKIT STM32MP1 by [bytes at work AG](https://www.bytesatwork.io).

## Usage

Use repo to download all necessary repositories:

	repo init -u https://github.com/bytesatwork/bsp-platform-st.git -b dunfell
	repo sync

When this commands completed successful, the following command will setup a
Yocto Project environment for byteDEVKIT STM32MP1:

	MACHINE=bytedevkit-stm32mp1 DISTRO=poky-bytesatwork EULA=1 . setup-environment build

The final command builds a minimal image:

	bitbake bytesatwork-minimal-image

The output is found in:

	tmp/deploy/images/bytedevkit-stm32mp1
