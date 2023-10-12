```go
package main

import (
	"encoding/json"
	"fmt"
)

type Human struct {
	Name        string                       `json:"name"`
	Pronouns    []string                     `json:"pronouns"`
	Education   string                       `json:"education"`
	Research    string                       `json:"research"`
	StudentOrgs string			 `json:"student_organizations"`
	Description string                       `json:"description"`
	Aliases     []string                     `json:"aliases"`
	Skills      map[string][]interface{}     `json:"skills"`
	Endpoints   map[string]map[string]string `json:"endpoints"`
	Hobbies     []string                     `json:"hobbies"`
}

func main() {
	me := Human{
		Name:        fmt.Sprintf("Raaj %s Patel", "T"),
		Pronouns:    []string{"he", "him"},
		Education:   "Electrical Engineering B.S. @ Texas A&M University",
		Research:    "Computer Engineering",
		StudentOrgs: "Formula SAE Electric",
		Description: "Currently working as a contract software engineer. Texas A&M Formula SAE EV Battery Subteam Member '24.",
		Aliases:     []string{"Raajheer1", "Raaj Patel", "Raaj"},
		Skills: map[string][]interface{}{
			"go": {
				"Gin", "Gorm", "gRPC",
			},
			"python": {
				"BeautifulSoup", "scikit-learn", "TensorFlow",
			},
			"javascript": {
				"NodeJS", "VueJS", "Typescript",
			},
			"c++": {},
			"html&css": {
				"Bootstrap4", "SCSS", "CSS", "TailwindCSS",
			},
			"devops": {
				"K3s", "Docker", "Github Actions", "Kustomize", "ArgoCD",
			},
			"other": {
				"MySQL", "MongoDB", "RabbitMQ",
			},
		},
		Endpoints: map[string]map[string]string{
			"Discord": {
				"username":      "Raaj Patel",
				"discriminator": "7762",
			},
			"Email": {
				"username": "the",
				"domain":   "raajpatel.dev",
			},
		},
		Hobbies: []string{
			"Programming", "Aviation", "Semiconductors", "Cryptography",
		},
	}

	user, err := json.MarshalIndent(me, "", "  ")
	if err != nil {
		fmt.Println("Uh oh! Something went wrong... Maybe 'Raaj Patel' is not of the Human Species!")
		return
	}

	fmt.Println(string(user))
}

```
