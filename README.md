function insertionSort(arr) {
    // Parcourir le tableau à partir du deuxième élément
    for (let i = 1; i < arr.length; i++) {
        // L'élément à insérer
        let key = arr[i];
        // Index du dernier élément de la séquence triée
        let j = i - 1;

        // Déplacer les éléments de arr[0..i-1] qui sont supérieurs à key
        // vers une position en avant de leur position actuelle
        while (j >= 0 && arr[j] > key) {
            arr[j + 1] = arr[j];
            j--;
        }
        // Insérer l'élément key à sa position correcte
        arr[j + 1] = key;
    }
    return arr;
}

// Exemple d'utilisation
const array = [5, 2, 9, 1, 5, 6];
console.log("Tableau avant le tri:", array);
const sortedArray = insertionSort(array);
console.log("Tableau après le tri:", sortedArray);
