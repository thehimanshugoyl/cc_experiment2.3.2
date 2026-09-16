# cc_experiment2.3.2
# javascript

var findDuplicate = function(nums) {
    let slow = nums[0];
    let fast = nums[0];

    // Find intersection point
    do {
        slow = nums[slow];
        fast = nums[nums[fast]];
    } while (slow !== fast);

    // Find entrance of cycle
    slow = nums[0];

    while (slow !== fast) {
        slow = nums[slow];
        fast = nums[fast];
    }

    return slow;
};
