# Gamer Velocity

## Example Code for Average Movement Velocity of R.Arm
```
# calculate the average velocity for each body part
avg_vx_wrist = np.mean(vx_wrist_smoothed)
avg_vx_elbow = np.mean(vx_elbow_smoothed)
avg_vx_shoulder = np.mean(vx_shoulder_smoothed)

print(f"Average wrist velocity: {avg_vx_wrist:.2f} cm/sec")
print(f"Average elbow velocity: {avg_vx_elbow:.2f} cm/sec")
print(f"Average shoulder velocity: {avg_vx_shoulder:.2f} cm/sec")
```

## Average Movement Velocity of R.Arm (Plot)
<p align="center">
<img width="500" height="350" src=images/gamer_velocity.png
</p>

## Example Code for Movement Velocity of R.Arm (Plot)
```
# create a new figure
fig, ax = plt.subplots()

# plot wrist velocity
ax.plot(df.index[1:-1], vx_wrist[1:-1], label='Wrist Velocity')

# plot elbow velocity
ax.plot(df.index[1:-1], vx_elbow[1:-1], label='Elbow Velocity')

# plot shoulder velocity
ax.plot(df.index[1:-1], vx_shoulder[1:-1], label='Shoulder Velocity')

# set axis labels and legend
ax.set_xlabel('Time (frames)')
ax.set_ylabel('Velocity (cm/sec)')
ax.legend()

# show the plot
plt.show()
```
