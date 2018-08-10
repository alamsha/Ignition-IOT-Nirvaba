# Ignition-IOT-Nirvana
This Ignition project can serve 15,000 dynamic tags from transaction groups as JSON api. You can add 1000's of tags to the transaction group and serve them as JSON payload.
1. Install SimpleTagProvider-unsigned.modl.
   (This module is built from Ignition SDK example)
2. This will automatically create 50,000 dynamic tags
3. ignition_group1.php will serve 1000 dynamic tags as JSON api.

To enable unsigned modules in ignition, just add the last line in your ignition.conf.

      # Java Additional Parameters
      wrapper.java.additional.1=-XX:+UseConcMarkSweepGC
      wrapper.java.additional.2=-XX:+CMSClassUnloadingEnabled
      wrapper.java.additional.3=-Ddata.dir=/var/lib/ignition/data
      wrapper.java.additional.4=-Dorg.apache.catalina.loader.WebappClassLoader.ENABLE_CLEAR_REFERENCES=false
      #wrapper.java.additional.5=-Xdebug
      #wrapper.java.additional.6=-Xrunjdwp:transport=dt_socket,server=y,suspend=n,address=8000
      
      wrapper.java.additional.7=-Dignition.allowunsignedmodules=true

