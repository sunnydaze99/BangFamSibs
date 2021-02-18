# BangFamSibs
import json
import requests


def sendToDiscord(webhook_url, message):
    """
    Post a message to discord API via a Webhook.
    """
    payload = {
        "come watch me play Little Nightmares 1 in vc HORROR": message
    }
    headers = {
        'Content-Type': 'application/json',
    }
    response = requests.post(webhook_url, data=json.dumps(payload), headers=headers)
    return response
