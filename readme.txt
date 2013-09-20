set AXIS_HOME=/home/mayuran/softwares/axis/axis-1_4
set AXIS_LIB=$AXIS_HOME/lib
set AXISCLASSPATH=$AXIS_LIB/axis.jar:$AXIS_LIB/commons-discovery.jar:$AXIS_LIB/commons-logging.jar:$AXIS_LIB/jaxrpc.jar:$AXIS_LIB/saaj.jar:$AXIS_LIB/log4j-1.2.8.jar:$AXIS_LIB/xml-apis.jar:$AXIS_LIB/xercesImpl.jar:$AXIS_LIB/wsdl4j.jar
export AXIS_HOME
export AXIS_LIB
export AXISCLASSPATH

java -cp $AXISCLASSPATH org.apache.axis.client.AdminClient -lhttp://localhost:8080/axisattachmentservice/services/AdminService attachdeploy.wsdd

java -d64 -classpath ".:/home/mayuran/softwares/axis/axis-1_4/lib/*" org.apache.axis.client.AdminClient -lhttp://localhost:8080/axisattachmentservice/services/AdminService attachdeploy.wsdd