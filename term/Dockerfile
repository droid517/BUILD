FROM gradle:8.9
RUN apt update
RUN apt install -y sdkmanager
ENV ANDROID_HOME=/usr/lib/android-sdk
RUN yes | sdkmanager --licenses
RUN git clone https://github.com/droid517/term.git /tmp/app
WORKDIR /tmp/app
RUN gradle clean
RUN gradle build
CMD term/build/outputs/apk/release/term-release-unsigned.apk
