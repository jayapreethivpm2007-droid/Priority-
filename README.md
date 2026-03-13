Hospital Emergency System (Patients Priority)


class PriorityQueue:

    def __init__(self):
        self.queue = []

    def insert(self, patient):
        self.queue.append(patient)

    def delete(self):
        max = 0
        for i in range(1, len(self.queue)):
            if self.queue[i][1] > self.queue[max][1]:
                max = i
        item = self.queue[max]
        del self.queue[max]
        return item

pq = PriorityQueue()

pq.insert(("Patient A",2))
pq.insert(("Patient B",5))
pq.insert(("Patient C",3))

print "Next Patient:", pq.delete()

Output:

Next Patient: ('Patient B', 5)
