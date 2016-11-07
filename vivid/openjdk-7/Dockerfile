FROM vicamo/android-pdk:vivid-openjdk-7

# 5C5364B55E51A24C: Launchpad PPA for Ubuntu Phablet Team
# C2518248EEA14886: Launchpad VLC
RUN echo "deb http://archive.ubuntu.com/ubuntu vivid multiverse" > /etc/apt/sources.list.d/vivid_multiverse.list \
	&& echo "deb-src http://archive.ubuntu.com/ubuntu vivid multiverse" >> /etc/apt/sources.list.d/vivid_multiverse.list \
	&& echo "deb http://archive.ubuntu.com/ubuntu vivid-updates multiverse" >> /etc/apt/sources.list.d/vivid_multiverse.list \
	&& echo "deb-src http://archive.ubuntu.com/ubuntu vivid-updates multiverse" >> /etc/apt/sources.list.d/vivid_multiverse.list \
	&& echo "deb http://archive.ubuntu.com/ubuntu vivid-security multiverse" >> /etc/apt/sources.list.d/vivid_multiverse.list \
	&& echo "deb-src http://archive.ubuntu.com/ubuntu vivid-security multiverse" >> /etc/apt/sources.list.d/vivid_multiverse.list \
	&& echo "deb http://ppa.launchpad.net/phablet-team/tools/ubuntu vivid main" > /etc/apt/sources.list.d/ppa.launchpad.net_phablet-team_vivid.list \
	&& apt-key adv --keyserver keyserver.ubuntu.com --recv-keys 5C5364B55E51A24C \
	&& apt-key adv --keyserver keyserver.ubuntu.com --recv-keys C2518248EEA14886 \
	&& apt-get update \
	&& apt-get install --no-install-recommends -y \
		abootimg \
		cpio \
		g++-4.8-multilib \
		imagemagick \
		kmod \
		libasound2-dev:i386 \
		libesd0-dev:i386 \
		libpulse-dev:i386 \
		openssh-client \
		phablet-tools \
		phablet-tools-citrain \
		pxz \
		software-properties-common \
		ubuntu-device-flash \
		ubuntu-emulator \
	&& apt-get clean \
	&& rm -f /var/lib/apt/lists/*_dists_*
