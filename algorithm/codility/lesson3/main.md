## FrogJmp
~~~java
public class Test4 {
	static public void main(String args[]) {
		System.out.println(new Test4().solution(1,1,3));
	}

	public int solution(int X, int Y, int D) {
		int returnVal = 0;
		Y = Y-X;
		if(D > Y) {
			if(Y==0){
				return 0;
			}else{
				return 1;
			}
			
		}else{
			returnVal = Y%D;
			if(returnVal ==0) {
				return (Y/D);
			}else {
				return (Y/D)+1;
			}
		}
    }
}
~~~

## TapeEquilibrium (score : 100)
~~~java
//�����Ʈ
//1. min���� �־��� ������ �ƴ� total������ ������
// total������ min���� �� ���, �迭�� ������ �� ��� total���� 0���ϰ� ���ü��� �ֱ� �빮��
// ������ �� �迭������ ��Ȯ�� ����  �ȳ��� �� �ִ�.
public class Test3 {
	static public void main(String args[]) {
		int A[] = {1,1 };
		System.out.println(new Test3().solution(A));
	}

	public int solution(int[] A) {
		// 1. �迭�� �� ���� ���Ѵ�.
		// 2. A[0]~ A[p-1]������ ���� ���Ѵ�.
		// 3. (1) - (2)���� min ���� ã�´�.

		int totalSum = 0;
		int aLenght = A.length;
		int min = 100001;
		
		int leftSum = 0;
		int rightSum = 0;
		for (int i = 0; i < aLenght; i++) {
			totalSum += A[i];
		}
		for (int i = 0; i < aLenght-1; i++) {
			leftSum += A[i];
			rightSum = totalSum-leftSum;
			if(min  > Math.abs(leftSum-rightSum )){
				min = Math.abs(leftSum-rightSum);
			}
		}
		return min;
	}
}


~~~

