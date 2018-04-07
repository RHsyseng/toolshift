# Tips & Tricks

## Openstack clients

- Download **clouds.yaml** file from the [UpShift tenant](https://rhos-ocp.infra.prod.upshift.eng.rdu2.redhat.com/dashboard/auth/login/?next=/dashboard/project/api_access/clouds.yaml/) (project > api_access > Download Openstack RC File)
- Put it on ~/.config/openstack/clouds.yaml
- Add _password: xxxxx_ and _verify: False_ to the clouds.yaml file
- Create this alias:
```
alias openstack='docker run -it --rm -v $PWD:/workspace -v ~/.config/openstack:/root/.config/openstack registry.gitlab.com/gbraad/openstack-client:centos openstack'
```
- Consume openstack with CLI:
```
openstack --os-cloud openstack network list
```
