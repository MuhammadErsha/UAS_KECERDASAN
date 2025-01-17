# UAS_KECERDASAN
class Node:
    def __init__(self, data):
        self.data = data
        self.children = []

    def add_child(self, child):
        self.children.append(child)

def build_tree(tree_data):
    nodes = {}
    for data in tree_data:
        nodes[data] = Node(data)

    for parent, children in tree_data.items():
        for child in children:
            nodes[parent].add_child(nodes[child])

    return nodes[list(tree_data.keys())[0]]

# Pohon 1
tree_data_1 = {
    'Hadi': ['Bayu', 'Desi', 'Wahyu', 'Rina', 'Ardi'],
    'Bayu': ['Fahrul', 'Tari'],
    'Desi': ['Nurul'],
    'Wahyu': ['Yanto'],
    'Rina': ['Hamzah', 'Eka'],
    'Ardi': ['Mira', 'Bastian', 'Ana'],
    'Fahrul': ['Wanda'],
    'Tari': [],
    'Nurul': ['Aji'],
    'Yanto': ['Gunawan'],
    'Hamzah': [],
    'Eka': [],
    'Mira': ['Anggun'],
    'Bastian': ['Boy'],
    'Ana': [],
    'Wanda': [],
    'Aji': [],
    'Gunawan': [],
    'Anggun': [],
    'Boy': []
}

tree_1 = build_tree(tree_data_1)

# Pohon 2
tree_data_2 = {
    '6': ['1', '2', '8', '3', '4'],
    '1': ['0', 'Tari'],
    '2': ['Nurul'],
    '8': ['Yanto'],
    '3': ['Hamzah', 'Eka'],
    '4': ['9', 'Bastian', '5'],
    '0': ['Wanda'],
    'Tari': [],
    'Nurul': ['Aji'],
    'Yanto': ['Gunawan'],
    'Hamzah': [],
    'Eka': [],
    '9': ['Anggun'],
    '  
