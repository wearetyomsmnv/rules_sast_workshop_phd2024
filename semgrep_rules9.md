rules:
id: digitalocean-pat
patterns: 
pattern-regex: (?i)\b(dop_v1_[a-f0-9]{64})(?:['|\"|\n|\r|\s|\x60|;]|$)
languages: [generic]
message: ”FYI”
severity: ERROR
