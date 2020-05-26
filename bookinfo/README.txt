run the following command to install & deploy the 'bookinfo' app:
        ansible-playbook main.yaml

ensure that red hat service mesh is already installed under the project name 'istio-system'

one way to verify is to visit http://$GATEWAY_URL/productpage

where $GATEWAY_URL can be set via this command:
        export GATEWAY_URL=$(oc -n istio-system get route istio-ingressgateway -o jsonpath='{.spec.host}')

