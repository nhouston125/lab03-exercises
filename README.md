Find All Duplicates

function findDups(nums) {
    const counts = {};
    const dups = [];

    nums.forEach(num => {
        counts[num] = (counts[num] || 0) + 1;
    });

    Object.entries(counts).forEach(([num, count]) => {
        if (count > 1) {
            dups.push(parseInt(num));
        }
    });

    return dups;
}