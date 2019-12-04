---
title: نظرة عامة على التوقيعات الإلكترونية
description: توفر هذه المقالة نظرة عامة على التواقيع الإلكترونية وتصف كيفية استخدامها.
author: maertenm
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SIGParameters, SIGProcSetup, SIGReasonCode
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 13611
ms.assetid: 98dc6b79-1895-45d8-9dd1-2c8a351b58af
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3d1d8952324bb16bcfa6a8b42fc4f157edb75cf1
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/18/2019
ms.locfileid: "2811283"
---
# <a name="electronic-signatures-overview"></a><span data-ttu-id="3fe7e-103">نظرة عامة على التوقيعات الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="3fe7e-103">Electronic signatures overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3fe7e-104">توفر هذه المقالة نظرة عامة على التواقيع الإلكترونية وتصف كيفية استخدامها.</span><span class="sxs-lookup"><span data-stu-id="3fe7e-104">This article provides an overview of electronic signatures and describes how they can be used.</span></span>

## <a name="what-is-an-electronic-signature"></a><span data-ttu-id="3fe7e-105">ما المقصود بالتوقيع الإلكتروني؟</span><span class="sxs-lookup"><span data-stu-id="3fe7e-105">What is an electronic signature?</span></span>

<span data-ttu-id="3fe7e-106">ويؤكد التوقيع الإلكتروني هوية الشخص الذي يكون على وشك البدء في عملية حساب أو الموافقة عليها.</span><span class="sxs-lookup"><span data-stu-id="3fe7e-106">An electronic signature confirms the identity of a person who is about to start or approve a computing process.</span></span> <span data-ttu-id="3fe7e-107">في بعض الصناعات، يعد التوقيع الإلكتروني ملزمًا قانونيًا كالتوقيع الكتابي.</span><span class="sxs-lookup"><span data-stu-id="3fe7e-107">In some industries, an electronic signature is as legally binding as a handwritten signature.</span></span>

<span data-ttu-id="3fe7e-108">يعد التوقيع الإلكتروني بمثابة شرط للامتثال للقوانين للعديد من الصناعات المنظمة، مثل المستحضرات الدوائية والأغذية والمشروبات والفضاء والدفاع.</span><span class="sxs-lookup"><span data-stu-id="3fe7e-108">Electronic signatures are a regulations compliance requirement for several regulated industries, such as pharmaceuticals, food and beverage, and aerospace and defense.</span></span> <span data-ttu-id="3fe7e-109">كما أنه مطلوب للالتزام بالقوانين الواردة بالجزء 11 من الباب 21 في مدونة القوانين الفيدرالية الصادرة عن إدارة الأغذية والأدوية (FDA) في الولايات المتحدة الأمريكية.</span><span class="sxs-lookup"><span data-stu-id="3fe7e-109">They are also required for compliance with regulations in 21 CFR Part 11 that was issued by the Food and Drug Administration (FDA) in the United States.</span></span>

> [!NOTE]
> <span data-ttu-id="3fe7e-110">لا يُعد التوقيع إلكتروني بحد ذاته مماثلاً للتوقيع الرقمي.</span><span class="sxs-lookup"><span data-stu-id="3fe7e-110">An electronic signature by itself isn't the same as a digital signature.</span></span> <span data-ttu-id="3fe7e-111">فالتوقيع الإلكتروني مجرد بديل عن التوقيع بخط اليد، حيث يوفر التوقيع الرقمي تدابير أمنية إضافية.</span><span class="sxs-lookup"><span data-stu-id="3fe7e-111">An electronic signature is just a substitute for a handwritten signature, whereas a digital signature provides additional security measures.</span></span> <span data-ttu-id="3fe7e-112">ويمكن أن يساعد التوقيع الرقمي في تحديد ما إذا كان مستخدم أو عملية أخرى قد عبثت بالبيانات.</span><span class="sxs-lookup"><span data-stu-id="3fe7e-112">A digital signature can help identify whether another user or process has tampered with the data.</span></span> <span data-ttu-id="3fe7e-113">كما يمكن التحقق من التوقع الرقمي، ولا يمكن دحض هذا التحقق من قِبل مالك الشهادة التي تم استخدامها للتوقيع على البيانات.</span><span class="sxs-lookup"><span data-stu-id="3fe7e-113">A digital signature can also be verified, and this verification can't be refuted by the owner of the certificate that was used to sign the data.</span></span> <span data-ttu-id="3fe7e-114">كما هو موضح أدناه، تشتمل التواقيع الإلكترونية على وظائف التوقيع الرقمي المضمنة.</span><span class="sxs-lookup"><span data-stu-id="3fe7e-114">As described below, electronic signatures have built-in digital signature functionality.</span></span>

## <a name="electronic-signatures"></a><span data-ttu-id="3fe7e-115">التوقيعات الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="3fe7e-115">Electronic signatures</span></span>

<span data-ttu-id="3fe7e-116">يمكنك استخدام التواقيع الإلكترونية للعمليات التجارية الحساسة.</span><span class="sxs-lookup"><span data-stu-id="3fe7e-116">You can use electronic signatures for critical business processes.</span></span> <span data-ttu-id="3fe7e-117">لدى بعض العمليات قدرات توقيع إلكتروني مضمنة.</span><span class="sxs-lookup"><span data-stu-id="3fe7e-117">Some processes have built-in electronic signature capabilities.</span></span> <span data-ttu-id="3fe7e-118">كما يمكنك إنشاء متطلبات التوقيع المخصص لأي جدول وحقل قاعدة بيانات.</span><span class="sxs-lookup"><span data-stu-id="3fe7e-118">You can also create custom signature requirements for any database table and field.</span></span>

<span data-ttu-id="3fe7e-119">تتميز التواقيع الإلكترونية بوظائف التوقيع الرقمي المضمنة.</span><span class="sxs-lookup"><span data-stu-id="3fe7e-119">Electronic signatures have built-in digital signature functionality.</span></span> <span data-ttu-id="3fe7e-120">يجب على كل مستخدم يوقع على المستندات الحصول على شهادة تشفير صالحة.</span><span class="sxs-lookup"><span data-stu-id="3fe7e-120">Every user who signs documents must obtain a valid cryptographic certificate.</span></span> <span data-ttu-id="3fe7e-121">وعند التوقيع على مستند، يتم التحقق من المفتاح الخاص المقترن بالشهادة.</span><span class="sxs-lookup"><span data-stu-id="3fe7e-121">When a document is signed, the private key that is associated with that certificate is validated.</span></span> <span data-ttu-id="3fe7e-122">يتم تسجيل معلومات التوقيع الإلكتروني في سجل لتوفير سجل مراجعة.</span><span class="sxs-lookup"><span data-stu-id="3fe7e-122">Electronic signature information is recorded in a log to provide an audit trail.</span></span> <span data-ttu-id="3fe7e-123">لإعداد التواقيع الإلكترونية، انظر [إعداد التواقيع الإلكترونية](tasks/set-up-electronic-signatures.md).</span><span class="sxs-lookup"><span data-stu-id="3fe7e-123">To set up electronic signatures, see [Set up electronic signatures](tasks/set-up-electronic-signatures.md).</span></span>

## <a name="users-who-require-access-to-electronic-signatures"></a><span data-ttu-id="3fe7e-124">المستخدمون الذين يتطلبون الوصول إلى التوقيعات الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="3fe7e-124">Users who require access to electronic signatures</span></span>

<span data-ttu-id="3fe7e-125">عادة ما يتطلب ثلاثة أنواع من المستخدمين وصولاً آمنًا إلى التوقيعات الإلكترونية: مسؤولو التوقيعات الإلكترونية والموقعون ومراجعو التوقيعات الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="3fe7e-125">Three kinds of users typically require security access to electronic signatures: electronic signature administrators, signers, and electronic signature auditors.</span></span>

### <a name="electronic-signature-administrator"></a><span data-ttu-id="3fe7e-126">مسؤول التوقيع الإلكتروني</span><span class="sxs-lookup"><span data-stu-id="3fe7e-126">Electronic signature administrator</span></span>

<span data-ttu-id="3fe7e-127">يقوم مسؤول التواقيع الإلكترونية بإعداد متطلبات التوقيع والمحددات العامة والمعتمدين ويتلقى تنبيهات عندما يتعذر التحقق من صحة التواقيع.</span><span class="sxs-lookup"><span data-stu-id="3fe7e-127">The electronic signature administrator sets up signature requirements, general parameters, and approvers, and receives alerts when signatures can't be verified.</span></span> <span data-ttu-id="3fe7e-128">حسب الإعدادات الافتراضية، يتمتع المستخدم الذي ينتمي إلى دور الأمان **مدير تكنولوجيا المعلومات‬**  بإذن إدارة التواقيع الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="3fe7e-128">By default, a user who belongs to the **Information technology manager** security role has permission to administer electronic signatures.</span></span>

### <a name="signer"></a><span data-ttu-id="3fe7e-129">الموقِّع</span><span class="sxs-lookup"><span data-stu-id="3fe7e-129">Signer</span></span>

<span data-ttu-id="3fe7e-130">يوفر الموقع توقيعًا إلكترونيًا للمستندات والعمليات التي تتطلب توقيعات.</span><span class="sxs-lookup"><span data-stu-id="3fe7e-130">A signer provides electronic signatures for documents and processes that require signatures.</span></span> <span data-ttu-id="3fe7e-131">حسب الإعدادات الافتراضية، يتمتع المستخدم الذي ينتمي إلى دور الأمان **مستخدم النظام** بإذن توقيع المستندات إلكترونيًا.</span><span class="sxs-lookup"><span data-stu-id="3fe7e-131">By default, a user who belongs to the **System user** security role has permission to sign documents electronically.</span></span>

> [!NOTE]
> <span data-ttu-id="3fe7e-132">قد يطلب الموقّع الحصول على أذونات إضافية قبل أن يتم منحه حق الوصول إلى البيانات المرتبطة بالمستند أو العملية التي يتم التوقيع عليها.</span><span class="sxs-lookup"><span data-stu-id="3fe7e-132">The signer might require additional permissions before access is granted to data that is related to the document or process that is being signed.</span></span> <span data-ttu-id="3fe7e-133">يجب أن يحصل المستخدم الذي يقوم بتغيير البيانات، ويتعين عليه بعد ذلك التوقيع على التغييرات، على إذن يسمح له بتغيير البيانات.</span><span class="sxs-lookup"><span data-stu-id="3fe7e-133">A user who changes data and must then sign for those changes must have permission to change the data.</span></span> <span data-ttu-id="3fe7e-134">أما المستخدم الذي يوقّع بالنيابة عن مستخدم آخر، فقد لا يحتاج إلى الوصول إلى البيانات.</span><span class="sxs-lookup"><span data-stu-id="3fe7e-134">A user who signs on behalf of another user might not require access to the data.</span></span> <span data-ttu-id="3fe7e-135">على سبيل المثال، المشرف الذي يوقع على تغييرات الموظف.</span><span class="sxs-lookup"><span data-stu-id="3fe7e-135">An example of this kind of user is a supervisor who signs for an employee's changes.</span></span>

### <a name="electronic-signature-auditor"></a><span data-ttu-id="3fe7e-136">مراجع التوقيع الإلكتروني</span><span class="sxs-lookup"><span data-stu-id="3fe7e-136">Electronic signature auditor</span></span>

<span data-ttu-id="3fe7e-137">يقوم مراجع التوقيع الإلكتروني بمراجعة سجل قاعدة البيانات وسجل مراجعة التوقيعات المتوفر من سجل قاعدة البيانات.</span><span class="sxs-lookup"><span data-stu-id="3fe7e-137">The electronic signature auditor reviews the database log and the signature review log that is available from the database log.</span></span> <span data-ttu-id="3fe7e-138">حسب الإعدادات الافتراضية، يتمتع المستخدم الذي ينتمي إلى دور الأمان **مدير تكنولوجيا المعلومات‬**  بإذن تدقيق التواقيع الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="3fe7e-138">By default, a user who belongs to the **Information technology manager** security role has permission to audit electronic signatures.</span></span>

<span data-ttu-id="3fe7e-139">في حالة استخدام دور مختلف عن **مدير تكنولوجيا المعلومات**، تحقق من تعيين الدور إلى الامتيازات التالية:</span><span class="sxs-lookup"><span data-stu-id="3fe7e-139">If you use a role other than **Information technology manager**, make sure that the role is assigned the following privileges:</span></span>

- <span data-ttu-id="3fe7e-140">عرض حالات فشل التوقيع الإلكتروني</span><span class="sxs-lookup"><span data-stu-id="3fe7e-140">View electronic signature failures</span></span>
- <span data-ttu-id="3fe7e-141">عرض سجل قاعدة البيانات</span><span class="sxs-lookup"><span data-stu-id="3fe7e-141">View database log</span></span>

## <a name="signing-documents-electronically"></a><span data-ttu-id="3fe7e-142">التوقيع على المستندات إلكترونيًا</span><span class="sxs-lookup"><span data-stu-id="3fe7e-142">Signing documents electronically</span></span>

### <a name="get-a-certificate"></a><span data-ttu-id="3fe7e-143">الحصول على شهادة</span><span class="sxs-lookup"><span data-stu-id="3fe7e-143">Get a certificate</span></span>

<span data-ttu-id="3fe7e-144">قبل التوقيع على المستندات إلكترونيًا، يجب أن تطلب شهادة.</span><span class="sxs-lookup"><span data-stu-id="3fe7e-144">Before you sign documents electronically, you must request a certificate.</span></span>

> [!NOTE]
> <span data-ttu-id="3fe7e-145">تُستخدم ميزات Microsoft SQL Server لإنشاء شهادات وتمكين التوقيع الإلكتروني.</span><span class="sxs-lookup"><span data-stu-id="3fe7e-145">Microsoft SQL Server features are used to create certificates and enable electronic signing.</span></span> <span data-ttu-id="3fe7e-146">لا حاجة إلى أي شهادة إضافية أو بنية تحتية للمفتاح العام (PKI).</span><span class="sxs-lookup"><span data-stu-id="3fe7e-146">No additional certificate or public key infrastructure (PKI) is required.</span></span>

<span data-ttu-id="3fe7e-147">عندما تطلب شهادة، يتم إنشاء مفتاح عام ومفتاح خاص لك.</span><span class="sxs-lookup"><span data-stu-id="3fe7e-147">When you request a certificate, a public key and a private key are created for you.</span></span> <span data-ttu-id="3fe7e-148">ويتم تشفير المفتاح الخاص باستخدام كلمة مرور تعرفها أنت فقط.</span><span class="sxs-lookup"><span data-stu-id="3fe7e-148">The private key is encrypted by using a password that is known only to you.</span></span> <span data-ttu-id="3fe7e-149">وعندما توقّع على المستند إلكترونيًا، يتم التحقق من هويتك عندما تدخل كلمة المرور.</span><span class="sxs-lookup"><span data-stu-id="3fe7e-149">When you sign a document electronically, your identity is verified when you enter the password.</span></span>

<span data-ttu-id="3fe7e-150">لطلب شهادة، في الصفحة **خيارات**، على علامة تبويب **الحسابات**، انقر فوق **الحصول على شهادة**.</span><span class="sxs-lookup"><span data-stu-id="3fe7e-150">To request a certificate, on the **Options** page, on the **Accounts** tab, click **Get certificate**.</span></span>

<span data-ttu-id="3fe7e-151">يجب إدخال وتأكيد كلمة المرور التي ستستخدمها للتوقيع.</span><span class="sxs-lookup"><span data-stu-id="3fe7e-151">You must enter and confirm the password that you will use for signing.</span></span> <span data-ttu-id="3fe7e-152">يتم استخدام كلمة مرور لحماية مفتاحك الخاص وتخويل استخدام شهادتك.</span><span class="sxs-lookup"><span data-stu-id="3fe7e-152">The password is used to protect your private key and authorize the use of your certificate.</span></span> <span data-ttu-id="3fe7e-153">لا يتم تخزين كلمة المرور هذه في قاعدة البيانات، ولن تكون متوفرة لأي شخص آخر، ولا حتى المسؤول.</span><span class="sxs-lookup"><span data-stu-id="3fe7e-153">This password isn't stored in the database, and it isn't available to anyone else, not even to the administrator.</span></span>

<span data-ttu-id="3fe7e-154">إذا نسيت كلمة المرور التي ترتبط بالشهادة، فيجب إعادة تعيين تلك الشهادة.</span><span class="sxs-lookup"><span data-stu-id="3fe7e-154">If you forget the password that is connected with your certificate, that certificate must be reset.</span></span> <span data-ttu-id="3fe7e-155">إذا قمت بإعادة تعيين الشهادة، فلن تؤثر على المستندات التي وقّعت عليها باستخدام الشهادة السابقة.</span><span class="sxs-lookup"><span data-stu-id="3fe7e-155">If you reset the certificate, you don't affect documents that you signed by using the previous certificate.</span></span> <span data-ttu-id="3fe7e-156">لإعادة تعيين الشهادة، في الصفحة **خيارات**، انقر فوق **إعادة تعيين شهادة**.</span><span class="sxs-lookup"><span data-stu-id="3fe7e-156">To reset the certificate, on the **Options** page, click **Reset certificate**.</span></span>

### <a name="sign-a-document-electronically"></a><span data-ttu-id="3fe7e-157">توقيع مستند إلكترونيًا</span><span class="sxs-lookup"><span data-stu-id="3fe7e-157">Sign a document electronically</span></span>

<span data-ttu-id="3fe7e-158">تظهر صفحة **توقيع المستند‬** عندما تقوم بإجراء تغيير يتطلب توقيعًا إلكترونيًا.</span><span class="sxs-lookup"><span data-stu-id="3fe7e-158">The **Sign document** page is displayed when you make a change that requires an electronic signature.</span></span>

1. <span data-ttu-id="3fe7e-159">في صفحة **توقيع المستند**، انقر فوق علامة تبويب **المستند** لمراجعة التغييرات في المستند.</span><span class="sxs-lookup"><span data-stu-id="3fe7e-159">On the **Sign document** page, click the **Document** tab to review the changes to the document.</span></span>
2. <span data-ttu-id="3fe7e-160">في علامة التبويب **التوقيع**، حدد كود السبب.</span><span class="sxs-lookup"><span data-stu-id="3fe7e-160">On the **Signature** tab, select a reason code.</span></span>
3. <span data-ttu-id="3fe7e-161">أدخل تعليقًا، إذا كان التعليق مطلوبًا.</span><span class="sxs-lookup"><span data-stu-id="3fe7e-161">Enter a comment, if a comment is required.</span></span>
4. <span data-ttu-id="3fe7e-162">إذا لم يظهر معرف المستخدم في حقل **الموقِّع‬**، فحدده من القائمة.</span><span class="sxs-lookup"><span data-stu-id="3fe7e-162">If your user ID doesn't appear in the **Signer** field, select it in the list.</span></span>
5. <span data-ttu-id="3fe7e-163">أدخل موقعك، إذا كانت هذه المعلومات مطلوبة.</span><span class="sxs-lookup"><span data-stu-id="3fe7e-163">Enter your location, if this information is required.</span></span>
6. <span data-ttu-id="3fe7e-164">وانقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="3fe7e-164">Click **OK**.</span></span>

### <a name="sign-for-another-users-changes"></a><span data-ttu-id="3fe7e-165">التوقيع لتغييرات مستخدم آخر</span><span class="sxs-lookup"><span data-stu-id="3fe7e-165">Sign for another user's changes</span></span>

<span data-ttu-id="3fe7e-166">في بعض الأوقات، قد تريد أن يقوم أحد المستخدمين بالتوقيع على تغييرات قام بها مستخدم آخر.</span><span class="sxs-lookup"><span data-stu-id="3fe7e-166">Occasionally, you might want a user to sign for another user's changes.</span></span> <span data-ttu-id="3fe7e-167">على سبيل المثال، قد يُطلب من المشرف التوقيع على التغييرات التي قام بها أحد الموظفين على قائمة مكونات الصنف.</span><span class="sxs-lookup"><span data-stu-id="3fe7e-167">For example, a supervisor might be required to sign for changes that an employee makes to a bill of materials (BOM).</span></span> <span data-ttu-id="3fe7e-168">استخدم هذا الإجراء لتفويض مستخدم كموقّع لمستخدم آخر.</span><span class="sxs-lookup"><span data-stu-id="3fe7e-168">Use this procedure to designate a user as a signer for another user.</span></span>

> [!NOTE]
> <span data-ttu-id="3fe7e-169">وعندما يقوم مستخدم بالتوقيع لتغيير قام به مستخدم آخر، يجب تزويد التوقيع في محطة العمل الخاصة بالمستخدم الذي قام بإجراء التغيير.</span><span class="sxs-lookup"><span data-stu-id="3fe7e-169">When one user signs for another user's change, the signature must be provided at the workstation of the user who made the change.</span></span> <span data-ttu-id="3fe7e-170">ولا يمكن للمستخدم حفظ التغيير حتى يتم توفير التوقيع.</span><span class="sxs-lookup"><span data-stu-id="3fe7e-170">The user can't save the change until the signature has been provided.</span></span>

<span data-ttu-id="3fe7e-171">لتعيين المعتمدين‬، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="3fe7e-171">To designate approvers, follow these steps.</span></span>

1. <span data-ttu-id="3fe7e-172">في الصفحة **خيارات**، على علامة تبويب **الحسابات**، انقر فوق **تعيين معتمد**.</span><span class="sxs-lookup"><span data-stu-id="3fe7e-172">On the **Options** page, on the **Accounts** tab, click **Designate approver**.</span></span>
2. <span data-ttu-id="3fe7e-173">في حقل **معرف المستخدم المعتمد‬**، حدد معرف المستخدم الذي يجب أن يوقّع على تغييرات مستخدم آخر.</span><span class="sxs-lookup"><span data-stu-id="3fe7e-173">In the **Approver user ID** field, select the ID of the user who must sign for another user's changes.</span></span>
3. <span data-ttu-id="3fe7e-174">في الحقل **التوقيع لمعرف المستخدم**، حدد معرف المستخدم الذي يجب التوقيع على التغييرات التي قام بها.</span><span class="sxs-lookup"><span data-stu-id="3fe7e-174">In the **Sign for user ID** field, select the ID of the user whose changes must be signed for.</span></span>
