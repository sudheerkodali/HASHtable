# HASHtable
DAS HASH table intro

class HashTable {
  constructor(capacity) {
    this.capacity = capacity;
    this.table = new Array(capacity);
  }

  hash(key) {
    return key % this.capacity;
  }

  put(key, value) {
    index = this.hash(key);
    this.table[index] = value;
  }

  get(key) {
    index = this.hash(key);
    return this.table[index];
  }

  __len__() {
    return this.table.length;
  }
}

if (name === "main") {
  const hash_table = new HashTable(10);
  hash_table.put("TOYOTA", "Car");
  hash_table.put("TESLA", "Car");
  hash_table.put("TATA", "Car");

  console.log(hash_table.get("TOYOTA")); // Car
  console.log(hash_table.get("TESLA")); // Car
  console.log(hash_table.get("TATA")); // Car
  console.log(hash_table.length); // 3
}
