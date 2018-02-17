# fill_matrix
螺旋填充矩阵
PAT 的螺旋矩阵的填充
难点在于填充矩阵
本想着缩小区间就可以了然而并不是。。。
int c = 0, d = 0, i = 0;
	int bod1 = 0, bod2 = 0,bod3 = a-1,bod4 = b-1;
	k[0][0] = p[i++];
	while (i < p.size()) {
		while (d < bod3) k[c][++d] = p[i++];
		bod3--;
		while (c < bod4) k[++c][d] = p[i++];
		bod4--;
		while (d > bod1) k[c][--d] = p[i++];
		bod1++;
		while (c > bod2+1) k[--c][d] = p[i++];
		bod2++;
	}
  这是第一个算法 发现遇到素数第四步就出现了问题因为只有一列所以实际上在第四个while i 已经越界了所以会出错
  笔记就是好用写几句就有想法了
  加了个条件就AC了
  年初二再搞一题贪心
