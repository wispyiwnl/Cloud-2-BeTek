## Auto Scaling Group


![LaunchTemplate](../media/mar16/LaunchTemplate.png)

![AutoScalingGroups](../media/mar16/AutoScalingGroups.png)

![AutoScalingGroups](../media/mar16/AutoScalingGroups1.png)

![AutoScalingGroups](../media/mar16/AutoScalingGroups2.png)


## CloudWatch

![CloudWatchExamen](../media/mar16/CloudWatchExamen.png)

![CloudWatchExamen](../media/mar16/CloudWatchExamen1.png)

![CloudWatchExamen](../media/mar16/CloudWatchExamen90.png)

![CloudWatchExamen](../media/mar16/CloudWatchExamen2.png)

## CloudTrail

![CloudTrail](../media/mar16/CloudTrail.png)


<details>
<summary>JSON</summary>

```json
{
    "eventVersion": "1.11",
    "userIdentity": {
        "type": "AssumedRole",
        "principalId": "AROAZQ3DSS4VILINXU7ZK:AutoScaling",
        "arn": "arn:aws:sts::654654478122:assumed-role/AWSServiceRoleForAutoScaling/AutoScaling",
        "accountId": "654654478122",
        "accessKeyId": "ASIAZQ3DSS4VHDZDJXHR",
        "sessionContext": {
            "sessionIssuer": {
                "type": "Role",
                "principalId": "AROAZQ3DSS4VILINXU7ZK",
                "arn": "arn:aws:iam::654654478122:role/aws-service-role/autoscaling.amazonaws.com/AWSServiceRoleForAutoScaling",
                "accountId": "654654478122",
                "userName": "AWSServiceRoleForAutoScaling"
            },
            "attributes": {
                "creationDate": "2026-03-17T00:59:40Z",
                "mfaAuthenticated": "false"
            }
        },
        "invokedBy": "autoscaling.amazonaws.com"
    },
    "eventTime": "2026-03-17T00:59:42Z",
    "eventSource": "ec2.amazonaws.com",
    "eventName": "RunInstances",
    "awsRegion": "us-east-1",
    "sourceIPAddress": "autoscaling.amazonaws.com",
    "userAgent": "autoscaling.amazonaws.com",
    "requestParameters": {
        "instancesSet": {
            "items": [
                {
                    "minCount": 1,
                    "maxCount": 1
                }
            ]
        },
        "blockDeviceMapping": {},
        "availabilityZone": "us-east-1d",
        "monitoring": {
            "enabled": false
        },
        "subnetId": "subnet-0b2fbf6da06d9ba4b",
        "disableApiTermination": false,
        "disableApiStop": false,
        "clientToken": "e40673e5-38f7-16b1-c435-d81e1a99111a",
        "tagSpecificationSet": {
            "items": [
                {
                    "resourceType": "instance",
                    "tags": [
                        {
                            "key": "aws:autoscaling:groupName",
                            "value": "practica-asg-santiagorojas"
                        }
                    ]
                }
            ]
        },
        "launchTemplate": {
            "launchTemplateId": "lt-03a70e6a9f2f6657d",
            "version": "1"
        }
    },
    "responseElements": {
        "requestId": "0f6b158f-ee18-43ca-b0d8-c06657fb5abb",
        "reservationId": "r-0a33d6db14adc9189",
        "ownerId": "654654478122",
        "groupSet": {},
        "instancesSet": {
            "items": [
                {
                    "instanceId": "i-047be45c593a7157f",
                    "imageId": "ami-0f3caa1cf4417e51b",
                    "bootMode": "uefi-preferred",
                    "currentInstanceBootMode": "legacy-bios",
                    "instanceState": {
                        "code": 0,
                        "name": "pending"
                    },
                    "privateDnsName": "ip-000-00-00-000.ec2.internal",
                    "operator": {
                        "managed": false
                    },
                    "amiLaunchIndex": 0,
                    "productCodes": {},
                    "instanceType": "t2.micro",
                    "launchTime": 1773709181000,
                    "placement": {
                        "availabilityZone": "us-east-1d",
                        "availabilityZoneId": "use1-az6",
                        "tenancy": "default"
                    },
                    "monitoring": {
                        "state": "disabled"
                    },
                    "subnetId": "subnet-0b2fbf6da06d9ba4b",
                    "vpcId": "vpc-00f479057476a2db8",
                    "privateIpAddress": "000.00.00.000",
                    "stateReason": {
                        "code": "pending",
                        "message": "pending"
                    },
                    "architecture": "x86_64",
                    "rootDeviceType": "ebs",
                    "rootDeviceName": "/dev/xvda",
                    "blockDeviceMapping": {},
                    "virtualizationType": "hvm",
                    "hypervisor": "xen",
                    "tagSet": {
                        "items": [
                            {
                                "key": "aws:ec2launchtemplate:id",
                                "value": "lt-03a70e6a9f2f6657d"
                            },
                            {
                                "key": "aws:ec2launchtemplate:version",
                                "value": "1"
                            },
                            {
                                "key": "aws:autoscaling:groupName",
                                "value": "practica-asg-santiagorojas"
                            }
                        ]
                    },
                    "clientToken": "e40673e5-38f7-16b1-c435-d81e1a99111a",
                    "groupSet": {
                        "items": [
                            {
                                "groupId": "sg-01962fa2b69e1616c",
                                "groupName": "default"
                            }
                        ]
                    },
                    "sourceDestCheck": true,
                    "networkInterfaceSet": {
                        "items": [
                            {
                                "networkInterfaceId": "eni-021cf26efaa81d057",
                                "subnetId": "subnet-0b2fbf6da06d9ba4b",
                                "vpcId": "vpc-00f479057476a2db8",
                                "ownerId": "654654478122",
                                "operator": {
                                    "managed": false
                                },
                                "status": "in-use",
                                "macAddress": "0e:9c:6d:63:60:67",
                                "privateIpAddress": "000.00.00.000",
                                "privateDnsName": "ip-000-00-00-000.ec2.internal",
                                "sourceDestCheck": true,
                                "interfaceType": "interface",
                                "groupSet": {
                                    "items": [
                                        {
                                            "groupId": "sg-01962fa2b69e1616c",
                                            "groupName": "default"
                                        }
                                    ]
                                },
                                "attachment": {
                                    "attachmentId": "eni-attach-075438ba1844619f7",
                                    "deviceIndex": 0,
                                    "networkCardIndex": 0,
                                    "status": "attaching",
                                    "attachTime": 1773709181000,
                                    "deleteOnTermination": true
                                },
                                "privateIpAddressesSet": {
                                    "item": [
                                        {
                                            "privateIpAddress": "000.00.00.000",
                                            "privateDnsName": "ip-000-00-00-000.ec2.internal",
                                            "primary": true
                                        }
                                    ]
                                },
                                "ipv6AddressesSet": {},
                                "tagSet": {}
                            }
                        ]
                    },
                    "ebsOptimized": false,
                    "enaSupport": true,
                    "cpuOptions": {
                        "coreCount": 1,
                        "threadsPerCore": 1
                    },
                    "capacityReservationSpecification": {
                        "capacityReservationPreference": "open"
                    },
                    "enclaveOptions": {
                        "enabled": false
                    },
                    "metadataOptions": {
                        "state": "pending",
                        "httpTokens": "required",
                        "httpPutResponseHopLimit": 2,
                        "httpEndpoint": "enabled",
                        "httpProtocolIpv4": "enabled",
                        "httpProtocolIpv6": "disabled",
                        "instanceMetadataTags": "disabled"
                    },
                    "maintenanceOptions": {
                        "autoRecovery": "default",
                        "rebootMigration": "default"
                    },
                    "privateDnsNameOptions": {
                        "hostnameType": "ip-name",
                        "enableResourceNameDnsARecord": false,
                        "enableResourceNameDnsAAAARecord": false
                    }
                }
            ]
        },
        "requesterId": "661627717883"
    },
    "requestID": "0f6b158f-ee18-43ca-b0d8-c06657fb5abb",
    "eventID": "7513960c-90fe-48dd-b729-6671a6461e72",
    "readOnly": false,
    "resources": [
        {
            "accountId": "654654478122",
            "type": "AWS::EC2::Instance",
            "ARN": "arn:aws:ec2:us-east-1:654654478122:instance/i-047be45c593a7157f"
        }
    ],
    "eventType": "AwsApiCall",
    "managementEvent": true,
    "recipientAccountId": "654654478122",
    "eventCategory": "Management"
}
```
