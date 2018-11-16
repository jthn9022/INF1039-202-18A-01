graph = {}
graph["romeo"] = ["didier", "ibrahima"]
graph["didier"] = ["olaiton", "abbas"]
graph["ibrahima"] = ["dane", "cheik"]
graph["olaiton"] = ["abdel", "halima"]
graph["abbas"] = ["randah", "david"]
graph["dane"] = ["armand", "fabrice"]
graph["cheik"] = ["djouma", "etienne"]
graph["abdel"] = []
graph["halima"] = []
graph["randah"] = []
graph["david"] = []
graph["fabrice"] = []
graph["djouma"] = []
graph["etienne"] = []
graph["armand"] = []
def person_is_seller(name):
    if (name == "armand"):
        return True
    else :
        return False
from collections import deque
search_queue = deque()
search_queue += graph["romeo"] 
while search_queue:
    person = search_queue.popleft()
    if person_is_seller(person):
        print person + " is a mango seller!"
    else:
        search_queue += graph[person]
        print False
