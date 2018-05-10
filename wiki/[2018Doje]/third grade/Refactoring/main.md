## NCS����ڰ� �ʼ��ɷ´��� (�ڰ����� SW����_L3)
* ������� : �ڵ� �м� �� UI ����


* ���� ��ǥ
    1. �ҽ��ڵ尡 �����ϴ� ����� �����ϸ鼭 �ڵ� ������ �� ������ ������ �����ϵ��� �ڵ��� ������ ������ �� �ִ�.
    2. ��ȹ�� �ܼ�Ʈ�� �������� �����ΰ� ������ ���� ������, ����, ���̾� ������, �½�ũ �÷ο츦 ������ �� �ִ�.


* ��������
    1. ���ø����̼� �����丵
    2. UI ��Ű��ó ����

* �������� (���ø����̼� �����丵)
    1. ���� �ڵ� ǥ��
    2. ������ ����
    3. �����丵 ���
    4. �����丵 ���� ���
    5. ������ ǰ�� Ư��
    6. ������ ǰ�� Ư�� ���� ���
    7. �ڵ� ���� ����
    8. Ŭ�� �ڵ� Ư¡
    9. Ŭ�� �ڵ��� �ʿ伺 �� Ư¡
    10. ȸ�� �׽�Ʈ
--------

# ���� : Application Refactoring

### ����������
* ������ ���� (Design Patterns) �̶� ?
    * ��ü ���� ���α׷��� ���踦 �� �� ���� �߻��ϴ� �������� ���ϱ� ���� ���Ǵ� ����
    * ����� ���� ����Ʈ���� ���迡�� ���� ������ �������� ��� �� ���� ����(� ��Ȳ�� ������ ���� �ع�)
    * �Ϲ������� �ϳ��� ���Ͽ��� �װ��� ��Ұ� �ݵ�� �� �ִ�. &#128209; [��ó](https://wikidocs.net/580)
        1. �����̸�
        2. ���� : ���� ������ ����ϴ°��� �����ϸ� �ذ��� ������ �� ����� �����Ѵ�.
        3. �ع� : ���踦 �����ϴ� �� �ҵ�� �� ��ҵ� ���� ���� å�� �׸��� ���� ���踦 �����Ѵ�.
        4. ��� : ������ ������ �����ؼ� ��� ����� ������� �����Ѵ�.
    * ���� ���� (�߻� ��ü �ν��Ͻ�ȭ) &#128209; [��ó](http://seungdols.tistory.com/486)
    * ���� ���� (��ü ����) &#128209; [��ó](http://seungdols.tistory.com/487?category=652793)
    * ���� ����(��ü �� Ŀ�����̼�) &#128209; [��ó](http://seungdols.tistory.com/490?category=652793)
>>> [���� ���� : http://kyejusung.com/](http://kyejusung.com/2015/09/%EB%94%94%EC%9E%90%EC%9D%B8-%ED%8C%A8%ED%84%B4-1-strategy-pattern/)

### �����丵 ���
* Code smell or �ڵ��� ������ : ����Ʈ����� ������ �ƴ϶� �����̴�. �����ڳ� ��ȹ���� �ְ��� ���� ���� �ٲ�� �����̱� ������ �����丵�� ������ ��Ȯ�ϰ� ���������� �ʴ�.
    * Duplicated Code (�ߺ��ڵ�)
    * Long Method(��Ȳ�� �޼���)
    * Large Class (����� Ŭ����)
    * Long Parameter List  (������ �Ű�����)
    * Divergent Change (������ ���)
    * Shotgun Surgery (����� ����) &#128209; [��ó](http://http://blog.daum.net/bellosogno/10)
    * Feature Envy (�߸��� �Ҽ�)
    * Feature Envy (������ ��ġ)
    * Primitive Obsession (������ �⺻ Ÿ�� ���) &#128209; [��ó](http://blog.daum.net/bellosogno/13)
    * Switch Statement
    * Parallel Inheritance Hierarchies (���� ��� ����)
    * Lazy Class(�������� Ŭ����)
    * Speculative Generality(������ ���� �ڵ�) : Collapse Hierarchy + Inline Class
    * �ӽ� �ʵ�
    * Message Chains(�޽��� ü��) &#128209; [��ó](http://dj6316.torchpad.com/%EB%A6%AC%ED%8C%A9%ED%86%A0%EB%A7%81%28refactoring%29/CH.03+%EC%BD%94%EB%93%9C%EC%9D%98+%EA%B5%AC%EB%A6%B0%EB%82%B4/8.%EB%A9%94%EC%8B%9C%EC%A7%80+%EC%B2%B4%EC%9D%B8+Message+Chains)
    * Middle Man (���� �߰� �޼���) &#128209; [��ó](https://wikidocs.net/593)
    * Inappropriate Intimacy(����ģ ����) &#128209; [��ó](http://dj6316.torchpad.com/%EB%A6%AC%ED%8C%A9%ED%86%A0%EB%A7%81%28refactoring%29/CH.03+%EC%BD%94%EB%93%9C%EC%9D%98+%EA%B5%AC%EB%A6%B0%EB%82%B4/9.%EC%A7%80%EB%82%98%EC%B9%9C+%EA%B4%80%EC%97%AC+Inappropriate+Intimacy)
    * Alternative Class with Different Interfaces(�������̽��� �ٸ� ��� Ŭ����) &#128209; [��ó](http://dj6316.torchpad.com/%EB%A6%AC%ED%8C%A9%ED%86%A0%EB%A7%81%28refactoring%29/CH.03+%EC%BD%94%EB%93%9C%EC%9D%98+%EA%B5%AC%EB%A6%B0%EB%82%B4/9-1.%EC%9D%B8%ED%84%B0%ED%8E%98%EC%9D%B4%EC%8A%A4%EA%B0%80+%EB%8B%A4%EB%A5%B8+%EB%8C%80%EC%9A%A9+%ED%81%B4%EB%9E%98%EC%8A%A4+Alternative+Classes+with+Different+Interfaces)
    * Incomplete Library Class(������ ���̺귯�� Ŭ����)
    * ������ Ŭ����
    * Refuged Bequest(��ġ�� ��ӹ�)
    * ���ʿ��� �ּ�
>>> [���� ���� : https://wikidocs.net/](https://wikidocs.net/593)








