FROM amazonlinux as baseBox

WORKDIR /app

RUN yum -y install make gcc* zip
RUN curl --silent --location https://rpm.nodesource.com/setup_14.x | bash -
RUN yum -y install nodejs

####################
## SHARP LAYER BOX ##
####################
FROM baseBox as sharpLayerBox

COPY . .
COPY build.sh /build.sh
RUN ["ls", "-la"]
RUN ["chmod", "+x", "build.sh"]
CMD ["sh", "/build.sh"]
####################
## SHARP LAYER BOX ##
####################