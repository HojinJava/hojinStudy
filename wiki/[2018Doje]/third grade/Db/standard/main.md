## NCS����ڰ� �ʼ��ɷ´��� (�ڰ����� SW����_L3)
* ������� : DB ����ȭ


* ���� ��ǥ
    1. ���� ���� �������� �м��ϰ� ���ɰ��� ��ǥ�� �����ϸ� ���ɰ��� ���� ����� ����, ���ɰ��� ����, ���ɰ��� ����� ���������� ���ϸ�, �� �ܰ躰 ���⹰ �� ���� Ȱ���� ������ �� �ִ�.
    2. �����ͺ��̽� ����� ���� �ÿ� �ʿ��� ������ ���� ����� ��Ī, ����, ����, ��Ģ�� ���� ��å�� �����Ͽ� ������ �� �ִ�.


* �������� (�ҿ�ð�)
    1. �����ͺ��̽� ����Ȯ�� (40h)
        1. ���� �м��ϱ�
	2. ���� �����ϱ�
	3. ���ɰ������ ���ϱ�
    2. ������ ǥ��ȭ (20h)
        1. ������ ǥ��ȭ ��å�����ϱ�
	2. ������ ǥ�� �����ϱ�
	3. ������ ǥ�� �����ϱ�


* �������� (�����ͺ��̽� ����Ȯ��)
    1. ������ �𵨸� ���
    2. ������ ǥ�� ���� ���
    3. ������ ǥ�� ������ �����ϱ� ���� ���Ұ� ��� ������ ���� Ư��
    4. ������ ǥ�� ���μ����� ���� ����
    5. ������ ǥ��ȭ ���
    6. �����ͺ��̽� ���� ���
    7. ��ǥ �ý����� ǥ��ȭ ��å�� ���� Ư��
    8. ����Ͻ� �����ο� ���� ����
    9. ǥ�شܾ ���� ����
    10. ǥ�ص����ο� ���� ��Ģ
    11. ǥ�ؿ� ���� ����
    12. ǥ���ڵ忡 ���� ��Ģ
    13. ǥ��ȭ ��å ��ʿ� ����
    14. ǥ��ȭ ��å ����
    15. ǥ��ȭ ��ħ ����
--------

# ���� : Application Refactoring

### ����������
* ������ ���� (Design Patterns) �̶� ?
    * ��ü ���� ���α׷��� ���踦 �� �� ���� �߻��ϴ� �������� ���ϱ� ���� ���Ǵ� ����
    * ����� ���� ����Ʈ���� ���迡�� ���� ������ �������� ��� �� ���� ����(� ��Ȳ�� ������ ���� �ع�)
    * �Ϲ������� �ϳ��� ���Ͽ��� �װ��� ��Ұ� �ݵ�� �� �ִ�. [&#128209;](https://wikidocs.net/580)
        1. �����̸�
        2. ���� : ���� ������ ����ϴ°��� �����ϸ� �ذ��� ������ �� ����� �����Ѵ�.
        3. �ع� : ���踦 �����ϴ� �� �ҵ�� �� ��ҵ� ���� ���� å�� �׸��� ���� ���踦 �����Ѵ�.
        4. ��� : ������ ������ �����ؼ� ��� ����� ������� �����Ѵ�.
    * ���� ���� (�߻� ��ü �ν��Ͻ�ȭ) [&#128209;](http://seungdols.tistory.com/486)
    * ���� ���� (��ü ����) [&#128209;](http://seungdols.tistory.com/487?category=652793)
    * ���� ����(��ü �� Ŀ�����̼�) [&#128209;](http://seungdols.tistory.com/490?category=652793)
>>> [���� ���� : http://kyejusung.com/](http://kyejusung.com/2015/09/%EB%94%94%EC%9E%90%EC%9D%B8-%ED%8C%A8%ED%84%B4-1-strategy-pattern/)

### �����丵 ���
* Code smell or �ڵ��� ������ : ����Ʈ����� ������ �ƴ϶� �����̴�. �����ڳ� ��ȹ���� �ְ��� ���� ���� �ٲ�� �����̱� ������ �����丵�� ������ ��Ȯ�ϰ� ���������� �ʴ�.
    * Duplicated Code (�ߺ��ڵ�)
    * Long Method(��Ȳ�� �޼���)
    * Large Class (����� Ŭ����)
    * Long Parameter List  (������ �Ű�����)
    * Divergent Change (������ ���)
    * Shotgun Surgery (����� ����) [&#128209;](http://blog.daum.net/bellosogno/10)
    * Feature Envy (�߸��� �Ҽ�)
    * Feature Envy (������ ��ġ)
    * Primitive Obsession (������ �⺻ Ÿ�� ���) [&#128209;](http://blog.daum.net/bellosogno/13)
    * Switch Statement
    * Parallel Inheritance Hierarchies (���� ��� ����)
    * Lazy Class(�������� Ŭ����)
    * Speculative Generality(������ ���� �ڵ�) : Collapse Hierarchy + Inline Class
    * �ӽ� �ʵ�
    * Message Chains(�޽��� ü��) [&#128209;](http://dj6316.torchpad.com/%EB%A6%AC%ED%8C%A9%ED%86%A0%EB%A7%81%28refactoring%29/CH.03+%EC%BD%94%EB%93%9C%EC%9D%98+%EA%B5%AC%EB%A6%B0%EB%82%B4/8.%EB%A9%94%EC%8B%9C%EC%A7%80+%EC%B2%B4%EC%9D%B8+Message+Chains)
    * Middle Man (���� �߰� �޼���) [&#128209;](https://wikidocs.net/593)
    * Inappropriate Intimacy(����ģ ����) [&#128209;](http://dj6316.torchpad.com/%EB%A6%AC%ED%8C%A9%ED%86%A0%EB%A7%81%28refactoring%29/CH.03+%EC%BD%94%EB%93%9C%EC%9D%98+%EA%B5%AC%EB%A6%B0%EB%82%B4/9.%EC%A7%80%EB%82%98%EC%B9%9C+%EA%B4%80%EC%97%AC+Inappropriate+Intimacy)
    * Alternative Class with Different Interfaces(�������̽��� �ٸ� ��� Ŭ����) [&#128209;](http://dj6316.torchpad.com/%EB%A6%AC%ED%8C%A9%ED%86%A0%EB%A7%81%28refactoring%29/CH.03+%EC%BD%94%EB%93%9C%EC%9D%98+%EA%B5%AC%EB%A6%B0%EB%82%B4/9-1.%EC%9D%B8%ED%84%B0%ED%8E%98%EC%9D%B4%EC%8A%A4%EA%B0%80+%EB%8B%A4%EB%A5%B8+%EB%8C%80%EC%9A%A9+%ED%81%B4%EB%9E%98%EC%8A%A4+Alternative+Classes+with+Different+Interfaces)
    * Incomplete Library Class(������ ���̺귯�� Ŭ����) [&#128209;](http://dj6316.torchpad.com/%EB%A6%AC%ED%8C%A9%ED%86%A0%EB%A7%81%28refactoring%29/CH.03+%EC%BD%94%EB%93%9C%EC%9D%98+%EA%B5%AC%EB%A6%B0%EB%82%B4/10.%EB%AF%B8%ED%9D%A1%ED%95%9C+%EB%9D%BC%EC%9D%B4%EB%B8%8C%EB%9F%AC%EB%A6%AC+%ED%81%B4%EB%9E%98%EC%8A%A4+Incomplete+Library+Class)
    * ������ Ŭ����
    * Refuged Bequest(��ġ�� ��ӹ�)
    * ���ʿ��� �ּ�
>>> [���� ���� : https://wikidocs.net/](https://wikidocs.net/593)








