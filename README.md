plt.figure(figsize=(12, 7))

scatter = sns.scatterplot(
    data=combined,
    x='Total Transactions',
    y='Avg Customer Rating',
    hue='Salesperson',
    size='Total Transactions',
    sizes=(100, 500),
    palette='tab10',
    alpha=0.85
)

for _, row in combined.iterrows():
    plt.annotate(
        row['Salesperson'],
        xy=(row['Total Transactions'], row['Avg Customer Rating']),
        xytext=(6, 4),
        textcoords='offset points',
        fontsize=8.5,
        fontweight='bold'
    )

plt.axhline(y=combined['Avg Customer Rating'].mean(), color='red', linestyle='--', linewidth=1.2, label='Avg Rating')
plt.axvline(x=combined['Total Transactions'].mean(), color='blue', linestyle='--', linewidth=1.2, label='Avg Transactions')

plt.title('Customer Rating vs Total Transactions by Salesperson',
          fontsize=14, fontweight='bold', pad=15)
plt.xlabel('Total Transactions', fontsize=12)
plt.ylabel('Average Customer Rating', fontsize=12)
plt.ylim(0, 5.5)
plt.legend(bbox_to_anchor=(1.05, 1), loc='upper left', borderaxespad=0.)

plt.tight_layout()
plt.savefig('salesperson_scatterplot.png', dpi=150, bbox_inches='tight')
plt.show()
