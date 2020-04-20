#FROM plone:4.3.18
FROM plone:4.3.19


#RUN pip install --upgrade pip
#RUN pip install plone.app.jquerytools


COPY site.cfg /plone/instance/
RUN gosu plone buildout -c site.cfg

#ADD cModels.tgz /plone/instance/products
