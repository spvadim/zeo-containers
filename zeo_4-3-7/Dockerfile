#FROM plone:4.3.18
FROM plone:4.3.7


#RUN pip install --upgrade pip
#RUN pip install plone.app.jquerytools

USER root
#RUN apt-get update
#RUN apt-get install -yq sudo
RUN sed -i 's/http:\/\/pypi/https:\/\/pypi/g' /plone/buildout-cache/eggs/zc.buildout-2.4.3-py2.7.egg/zc/buildout/easy_install.py
USER plone

COPY site.cfg /plone/instance/
#RUN gosu plone buildout -c site.cfg
RUN bin/buildout -c site.cfg
