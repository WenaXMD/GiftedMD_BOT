[![Typing SVG](https://readme-typing-svg.demolab.com?font=Pacifico&pause=1000&multiline=true&width=435&lines=Welcome+%F0%9F%98%8A+to+GiftedMD_BOT+powered+by+wena_;Thanks+for+the+star+%F0%9F%8C%9F)](https://git.io/typing-svg)# GiftedMD_BOT
*Gifted MD* GitHub repo:  > ⚙️ *Gifted MD* is a smart messaging bot designed for automation, fast replies, and daily utilities. Built for smooth user experience, integration, and flexibility in digital communication. 

{
    "name": "Integration WhatsApp Business Cloud",
    "flow": [
        {
            "id": 1,
            "module": "whatsapp-business-cloud:sendMessage",
            "version": 1,
            "parameters": {
                "__IMTCONN__": 6762605
            },
            "mapper": {
                "fromId": "{{&}}",
                "to": "{{ignore}}{{erase}}{{false}}",
                "type": "text",
                "text": {
                    "body": "```📊 SYSTEM STATUS  - 🟢 Server Uptime: 100%  - 🔄 CPU Load: 41%  - 💾 Memory Usage: 2.3 GB / 4 GB  - 🔐 Firewall: Active  - 📡 Connection: Stable  \n👤 YOUR PROFILE  - Name: {name!}  - ID: WENA-00123  - Member Since: Jan 2024  - Current Plan: Premium  - Last Login: Today\n💰 ACCOUNT BALANCE  - Wallet Balance: KES 420.00  - Points: 135  - Last Transaction: +KES 200 (Top-up)  - Billing Method: M-Pesa  - Renewal: Auto-renew enabled```1. Previous Menu0. Main Menu",
                    "preview_url": true
                }
            },
            "metadata": {
                "designer": {
                    "x": -101,
                    "y": 131,
                    "messages": [
                        {
                            "category": "reference",
                            "severity": "error",
                            "message": "Invalid IML for parameter '{{&}}': Operator on beginning of an expression."
                        }
                    ]
                },
                "restore": {
                    "parameters": {
                        "__IMTCONN__": {
                            "label": "My WhatsApp Business Cloud connection",
                            "data": {
                                "scoped": "true",
                                "connection": "whatsapp-business-cloud"
                            }
                        }
                    },
                    "expect": {
                        "fromId": {
                            "mode": "edit"
                        },
                        "type": {
                            "label": "Text"
                        },
                        "text": {
                            "nested": {
                                "preview_url": {
                                    "mode": "chose"
                                }
                            }
                        }
                    }
                },
                "parameters": [
                    {
                        "name": "__IMTCONN__",
                        "type": "account:whatsapp-business-cloud,whatsapp-business-cloud2",
                        "label": "Connection",
                        "required": true
                    }
                ],
                "expect": [
                    {
                        "name": "fromId",
                        "type": "select",
                        "label": "Sender ID",
                        "required": true
                    },
                    {
                        "name": "to",
                        "type": "text",
                        "label": "Receiver",
                        "required": true
                    },
                    {
                        "name": "type",
                        "type": "select",
                        "label": "Message Type",
                        "required": true,
                        "validate": {
                            "enum": [
                                "text",
                                "image",
                                "audio",
                                "video",
                                "document",
                                "sticker",
                                "location",
                                "contacts",
                                "interactive"
                            ]
                        }
                    },
                    {
                        "name": "text",
                        "type": "collection",
                        "label": "Text",
                        "spec": [
                            {
                                "name": "body",
                                "type": "text",
                                "label": "Body",
                                "validate": {
                                    "max": 4096
                                },
                                "required": true
                            },
                            {
                                "name": "preview_url",
                                "type": "boolean",
                                "label": "Preview URL",
                                "required": true
                            }
                        ]
                    },
                    {
                        "name": "fromId",
                        "type": "select",
                        "label": "Sender ID",
                        "required": true
                    },
                    {
                        "name": "to",
                        "type": "text",
                        "label": "Receiver",
                        "required": true
                    },
                    {
                        "name": "type",
                        "type": "select",
                        "label": "Message Type",
                        "required": true,
                        "validate": {
                            "enum": [
                                "text",
                                "image",
                                "audio",
                                "video",
                                "document",
                                "sticker",
                                "location",
                                "contacts",
                                "interactive"
                            ]
                        }
                    },
                    {
                        "name": "text",
                        "type": "collection",
                        "label": "Text",
                        "spec": [
                            {
                                "name": "body",
                                "type": "text",
                                "label": "Body",
                                "validate": {
                                    "max": 4096
                                },
                                "required": true
                            },
                            {
                                "name": "preview_url",
                                "type": "boolean",
                                "label": "Preview URL",
                                "required": true
                            }
                        ]
                    }
                ]
            }
        }
    ],
    "metadata": {
        "instant": false,
        "version": 1,
        "scenario": {
            "roundtrips": 1,
            "maxErrors": 3,
            "autoCommit": true,
            "autoCommitTriggerLast": true,
            "sequential": false,
            "slots": null,
            "confidential": false,
            "dataloss": false,
            "dlq": false,
            "freshVariables": false
        },
        "designer": {
            "orphans": []
        },
        "zone": "us2.make.com",
        "notes": []
    }
}
