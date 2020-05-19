---
title: العمل مع الأصناف المتسلسلة في نقطة البيع
description: يوضح هذا الموضوع كيفيه إدارة الأصناف المتسلسلة في تطبيق نقطه البيع (POS).
author: boycezhu
manager: annbe
ms.date: 04/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: global
ms.author: boycezhu
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: 1e0d6aa7cd5576578378e70c6ee808833314aff3
ms.sourcegitcommit: 919620b4aca425e6a1248ee12f50a622d2531e58
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/27/2020
ms.locfileid: "3290760"
---
# <a name="work-with-serialized-items-in-the-pos"></a><span data-ttu-id="86f0e-103">العمل مع الأصناف المتسلسلة في نقطة البيع</span><span class="sxs-lookup"><span data-stu-id="86f0e-103">Work with serialized items in the POS</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="86f0e-104">يقوم العديد من بائعي التجزئة ببيع المنتجات التي تتطلب التحكم في الرقم التسلسلي.</span><span class="sxs-lookup"><span data-stu-id="86f0e-104">Many retailers sell products that require serial control.</span></span> <span data-ttu-id="86f0e-105">تتم الإشاره إلى هذه الأصناف بـ *الأصناف المتسلسلة*.</span><span class="sxs-lookup"><span data-stu-id="86f0e-105">These items are referred to as *serialized items*.</span></span> <span data-ttu-id="86f0e-106">قد يرغب بعض بائعي التجزئة في الحفاظ علي الأرقام التسلسلية لأغراض التعقب.</span><span class="sxs-lookup"><span data-stu-id="86f0e-106">Some retailers might want to maintain serial numbers for tracking purposes.</span></span> <span data-ttu-id="86f0e-107">وقد يرغب البائعون الآخرون في التقاط الأرقام التسلسلية أثناء عملية المبيعات، لأغراض الخدمة والضمان.</span><span class="sxs-lookup"><span data-stu-id="86f0e-107">Other retailers might want to capture serial numbers during the sales process, for service and warranty purposes.</span></span> <span data-ttu-id="86f0e-108">يوضح هذا الموضوع كيفيه إدارتك للأصناف المتسلسلة في تطبيق نقطه البيع (POS) بـ Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="86f0e-108">This topic explains how you can manage serialized items in the Microsoft Dynamics 365 Commerce point of sale (POS) application.</span></span>

## <a name="serial-number-configurations"></a><span data-ttu-id="86f0e-109">تكوينات الأرقام التسلسلية</span><span class="sxs-lookup"><span data-stu-id="86f0e-109">Serial number configurations</span></span>

<span data-ttu-id="86f0e-110">يعتبر الصنف صنفًا متسلسلاً إذا تم تعيينه لمجموعة أبعاد التعقب التي يتم إعدادها للسماح بالأرقام التسلسلية.</span><span class="sxs-lookup"><span data-stu-id="86f0e-110">An item is considered a serialized item if it's assigned a tracking dimension group that is set up to allow for serial numbers.</span></span> <span data-ttu-id="86f0e-111">في المقر الرئيسي لـ Commerce، على صفحة **مجموعات أبعاد التعقب** حدد خيار **نشط** لتمكين الأرقام التسلسلية لعملية المخزون.</span><span class="sxs-lookup"><span data-stu-id="86f0e-111">In Commerce headquarters, on the **Tracking dimension groups** page, select the **Active** option to enable serial numbers for the inventory process.</span></span> <span data-ttu-id="86f0e-112">لتمكين الأرقام التسلسلية لعمليه المبيعات، حدد خيار **نشط في عملية المبيعات**.</span><span class="sxs-lookup"><span data-stu-id="86f0e-112">To enable serial numbers for the sales process, select the **Active in sales process** option.</span></span>

<span data-ttu-id="86f0e-113">في علامة التبويب السريعة **بُعد التعقيب** إذا كان الخيار **‏‫مسموح بالإيصال الفارغ‬** في وضع التشغيل، فإن الرقم التسلسلي يعد إدخالا اختياريا خلال عملية استلام المخزون.</span><span class="sxs-lookup"><span data-stu-id="86f0e-113">On the **Tracking dimensions** FastTab, if the **Blank receipt allowed** option is turned on, the serial number is an optional input during the inventory receipt process.</span></span> <span data-ttu-id="86f0e-114">إذا كان هذا الخيار في وضع إيقاف التشغيل، فمن ثم يلزم توفير الرقم التسلسلي.</span><span class="sxs-lookup"><span data-stu-id="86f0e-114">If the option is turned off, the serial number is required.</span></span>

<span data-ttu-id="86f0e-115">في علامة التبيوب السريعة **الأرقام التسلسلية** ، إذا كان الخيار **‏‫التحكم في الرقم المسلسل‬** قيد التشغيل، فمن ثم يلزم أن يكون الرقم التسلسلي فريدًا لكل وحده.</span><span class="sxs-lookup"><span data-stu-id="86f0e-115">On the **Serial numbers** FastTab, if the **Serial number control** option is turned on, the serial number must be unique per unit.</span></span> <span data-ttu-id="86f0e-116">بمعنى آخر، لا يسمح بالأرقام التسلسلية المكررة.</span><span class="sxs-lookup"><span data-stu-id="86f0e-116">In other words, duplicated serial numbers aren't allowed.</span></span>

## <a name="serialized-items-in-the-receiving-process"></a><span data-ttu-id="86f0e-117">الأصناف المتسلسلة في عمليه الاستلام</span><span class="sxs-lookup"><span data-stu-id="86f0e-117">Serialized items in the receiving process</span></span>

<span data-ttu-id="86f0e-118">تتيح عملية **المخزون الداخلية** في تطبيق نقطة البيع للمستخدمين إجراء المهام التالية للأصناف المتسلسلة:</span><span class="sxs-lookup"><span data-stu-id="86f0e-118">The **Inbound inventory** operation in the POS application lets users perform the following tasks for serialized items:</span></span>

- <span data-ttu-id="86f0e-119">تسجيل الأرقام التسلسلية مقابل الأصناف المتسلسة عند استلام هذه الأصناف في المتجر من خلال أمر شراء.</span><span class="sxs-lookup"><span data-stu-id="86f0e-119">Register serial numbers against serialized items when those items are received in the store via a purchase order.</span></span>
- <span data-ttu-id="86f0e-120">التحقق من صحة الأرقام التسلسلية المُسجلة مسبقًا مقابل الأصناف المتسلسة عند استلام هذه الأصناف في المتجر من خلال أمر شراء أو أمر تحويل.</span><span class="sxs-lookup"><span data-stu-id="86f0e-120">Validate preregistered serial numbers against serialized items when those items are received in the store via a purchase order or transfer order.</span></span>

> [!NOTE]
> <span data-ttu-id="86f0e-121">لاستخدام عملية **المخزون الداخلية** لتسجيل أو للتحقق من صحة صنف متسلسل، يجب تعيين الصنف لمجموعة أبعاد تعقب للسماح بالأرقام المسلسلة للخيار **نشط** وليس خيار **نشط في عملية المبيعات**.</span><span class="sxs-lookup"><span data-stu-id="86f0e-121">To use the **Inbound inventory** operation to register or validate a serialized item, the item must be assigned a tracking dimension group that is set up to allow for serial numbers for the **Active** option, not the **Active in sales process** option.</span></span>

<span data-ttu-id="86f0e-122">لبدء عمليه الاستلام، في عملية **المخزون الداخلي** ، يمكنك البدء في طريقة العرض **الاستلام الآن** عن طريق مسح الكود الشريطي للصنف أو بإدخال معرف الصنف.</span><span class="sxs-lookup"><span data-stu-id="86f0e-122">To begin the receiving process, in the **Inbound inventory** operation, you can start in the **Receiving now** view by scanning the item bar code or entering the item ID.</span></span> <span data-ttu-id="86f0e-123">أو يمكنك البدء في طريقة العرض **قائمة الطلبات الكاملة** طريق تحديد الصنف يدويا.</span><span class="sxs-lookup"><span data-stu-id="86f0e-123">Alternatively, you can start in the **Full order list** view by manually selecting the item.</span></span>

<span data-ttu-id="86f0e-124">إذا كان الصنف الذي يتم تحديده أو استلامه عبارة عن عنصر متسلسل، فان جزء **التفاصيل** الخاص بالصنف سيحتوي على ارتباط **إدارة الرقم التسلسلي** الذي يفتح في صفحة **إدارة الأرقام التسلسلية**.</span><span class="sxs-lookup"><span data-stu-id="86f0e-124">If the item that is being selected or received is a serialized item, the **Details** pane for the item contains a **Manage serial number** link that opens the **Serial number management** page.</span></span> <span data-ttu-id="86f0e-125">أو، يمكنك فتح صفحة **إدارة الأرقام التسلسلية** وذلك إما بتحديد **التسلسلي** في شريط التطبيق الخاص بطريقة عرض تفاصيل الطلب أو بتحديد **إدارة الرقم التسلسلي** في مربع الحوار الذي يطالبك أثناء عملية الاستلام.</span><span class="sxs-lookup"><span data-stu-id="86f0e-125">Alternatively, you can open the **Serial number management** page either by selecting **Serial number** on the app bar of the order details view or by selecting **Manage serial number** in the dialog box that prompts you during the receiving process.</span></span> <span data-ttu-id="86f0e-126">تسر صفحة **إدارة الرقم التسلسلي** كافة بنود الأرقام المسلسلة المفتوحة التي تتنتظر التسجيل أو التحقق من صحتها.</span><span class="sxs-lookup"><span data-stu-id="86f0e-126">The **Serial number management** page lists all open serial number lines that are pending registration or validation.</span></span> <span data-ttu-id="86f0e-127">وقد توجد علامتا تبويب في هذه الصفحة: إحداهما للصنف الحالي والأخرى لكافة الأصناف المسلسلة في الأمر.</span><span class="sxs-lookup"><span data-stu-id="86f0e-127">There might be two tabs on this page: one for the current item and one for all the serialized items in the order.</span></span>

<span data-ttu-id="86f0e-128">يضم حقل **الحالة** في صفحة **إدارة الرقم التسلسلي** معلومات حول المرحلة الحالية التي يوجد فيها كل رقم تسلسلي:</span><span class="sxs-lookup"><span data-stu-id="86f0e-128">The **Status** field on the **Serial number management** page provides information about the current stage that each serial number is in:</span></span>

- <span data-ttu-id="86f0e-129">**غير مُسجل** – لم يتم تقديم الرقم المسلسل، أو لم يتم بعد التحقق من صحة الرقم المسلسل المُسجل مسبقًا.</span><span class="sxs-lookup"><span data-stu-id="86f0e-129">**Not registered** – The serial number hasn't been provided, or the preregistered serial number hasn't yet been validated.</span></span>
- <span data-ttu-id="86f0e-130">**قيد التسجيل** – تم تسجيل الرقم التسلسلي وحفظه محليا في قاعده بيانات القناة الخاصة بالمتجر، أو تم التحقق من صحة الرقم التسلسلي المُسجل مسبقًا.</span><span class="sxs-lookup"><span data-stu-id="86f0e-130">**Registering** – The serial number has been registered and saved locally to the store's channel database, or the preregistered serial number has been validated.</span></span> <span data-ttu-id="86f0e-131">سيتم إرسال الأرقام التسلسلية التي تكون حالتها " **قيد التسجيل** فقط إلى المقر الرئيسي لـ Commerce عند الانتهاء من الاستلام.</span><span class="sxs-lookup"><span data-stu-id="86f0e-131">Only serial numbers that have a status of **Registering** will be submitted to Commerce headquarters when you finish receiving.</span></span>

### <a name="register-serial-numbers-against-serialized-items"></a><span data-ttu-id="86f0e-132">تسجيل الأرقام التسلسلية مقابل الأصناف المتسلسلة</span><span class="sxs-lookup"><span data-stu-id="86f0e-132">Register serial numbers against serialized items</span></span>

<span data-ttu-id="86f0e-133">بالنسبة لأمر الشراء، فان مربع الحوار الذي يطالبك اثناء عمليه الاستلام لصنف مسلسل يعرض الخيار **إداره الرقم التسلسلي**.</span><span class="sxs-lookup"><span data-stu-id="86f0e-133">For a purchase order, a dialog box that prompts you during the receiving process of a serialized item offers the **Manage serial number** option.</span></span> <span data-ttu-id="86f0e-134">يمكنك تحديد هذا الخيار لفتح صفحة **إدارة الأرقام التسلسلية** والبدء في تسجيل الأرقام التسلسلية.</span><span class="sxs-lookup"><span data-stu-id="86f0e-134">You can select that option to open the **Serial number management** page and start to register serial numbers.</span></span> <span data-ttu-id="86f0e-135">يمكنك أيضا تخطي هذه الخطوة اثناء عمليه الاستلام وتقديم الإدخال لاحقا، قبل ترحيل الإيصال.</span><span class="sxs-lookup"><span data-stu-id="86f0e-135">You can also skip this step during the receiving process and provide the input later, before the receipt is posted.</span></span>

<span data-ttu-id="86f0e-136">افتراضيا، يتم عرض علامة التبويب الخاصة بالصنف الحالي.</span><span class="sxs-lookup"><span data-stu-id="86f0e-136">By default, the tab for the current item is shown.</span></span> <span data-ttu-id="86f0e-137">تحتوي كافة بنود الرقم التسلسلي على قيمه رقميه تسلسليه فارغة وحالة **غير مسجل**.</span><span class="sxs-lookup"><span data-stu-id="86f0e-137">All serial number lines have an empty serial number value and a status of **Not registered**.</span></span> <span data-ttu-id="86f0e-138">يمكنك مسح الأكواد الشريطية للأرقام المسلسلة، أو يمكنك تحديد **رقم تسلسلي** في شريط التطبيقات لإدخال الأرقام التسلسلية بشكل مستمر في مربع الحوار.</span><span class="sxs-lookup"><span data-stu-id="86f0e-138">You can scan serial number bar codes, or you can select **Serial number** on the app bar to continuously enter serial numbers in the dialog box.</span></span> <span data-ttu-id="86f0e-139">تظهر الأرقام التسلسلية التي تقوم بإدخالها في القائمة، ويتم تغيير حاله بنود الرقم التسلسلي إلى **قيد التسجيل**.</span><span class="sxs-lookup"><span data-stu-id="86f0e-139">The serial numbers that you enter appear in the list, and the status of the serial number lines is changed to **Registering**.</span></span> <span data-ttu-id="86f0e-140">الحد الأقصى لعدد الأرقام التسلسلية التي يمكنك تسجيلها في القائمة يساوي كميه الاستلام.</span><span class="sxs-lookup"><span data-stu-id="86f0e-140">The maximum number of serial numbers that you can register in the list equals the receiving quantity.</span></span> <span data-ttu-id="86f0e-141">إذا ارتكبت خطا ما، فيمكنك تحديد **تحرير** أو **مسح** في جزء **التفاصيل** لاجراء تغييرات على الأرقام التسلسلية التي قمت بإدخالها.</span><span class="sxs-lookup"><span data-stu-id="86f0e-141">If you make a mistake, you can select **Edit** or **Clear** in the **Details** pane to make changes to the serial numbers that you entered.</span></span>

<span data-ttu-id="86f0e-142">يمكنك أيضا تسجيل الأرقام التسلسلية على علامة تبويب **جميع الأصناف المتسلسلة** في صفحة **إدارة الأرقام التسلسلية**.</span><span class="sxs-lookup"><span data-stu-id="86f0e-142">You can also register serial numbers on the **All serialized items** tab of the **Serial number management** page.</span></span> <span data-ttu-id="86f0e-143">في هذه القائمة، حدد الصنف الذي تريد تسجيل أرقام متسلسلة مقابله.</span><span class="sxs-lookup"><span data-stu-id="86f0e-143">In the list, select the item that you want to register serial numbers against.</span></span>

<span data-ttu-id="86f0e-144">أثناء تسجيل الرقم التسلسلي في هذه الصفحة، يتم التحقق من الصحة مرتين.</span><span class="sxs-lookup"><span data-stu-id="86f0e-144">During serial number registration on this page, duplication validation occurs.</span></span> <span data-ttu-id="86f0e-145">إذا حاولت إدخال رقم متسلسل مكرر مقابل صنف تم تشغيل التحكم في الرقم التسلسلي له، فستتلقى رسالة خطأ ويجب أن يوفر رقما مختلفا.</span><span class="sxs-lookup"><span data-stu-id="86f0e-145">If you try to enter a duplicated serial number against an item that serial number control is turned on for, you receive an error message and must provide a different number.</span></span>

### <a name="validate-serial-numbers-on-serialized-items"></a><span data-ttu-id="86f0e-146">التحقق من صحة الأرقام التسلسلية على الأصناف المتسلسلة</span><span class="sxs-lookup"><span data-stu-id="86f0e-146">Validate serial numbers on serialized items</span></span>

<span data-ttu-id="86f0e-147">بالنسبة لأمر التحويل، يجب ان يُسجل الجانب الخارجي الأرقام التسلسلية مسبقًا في الأصناف المسلسلة أثناء عمليه الشحن.</span><span class="sxs-lookup"><span data-stu-id="86f0e-147">For a transfer order, the outbound side must preregister serial numbers on the serialized items during the shipment process.</span></span> <span data-ttu-id="86f0e-148">بالنسبة لأمر الشراء، قد يقدم المورد معلومات الرقم التسلسلي من خلال إشعار شحن مسبق (ASN)، كما يمكنك تسجيل الأرقام الموجودة مسبقًا في الأصناف التي سيتم شحنها.</span><span class="sxs-lookup"><span data-stu-id="86f0e-148">For a purchase order, the supplier might provide serial number information through an Advance Shipment Notice (ASN), and you can preregister the numbers on the items that will be shipped.</span></span> <span data-ttu-id="86f0e-149">وفي كلتا الحالتين، تكون الأرقام التسلسلية معروفه قبل عمليه الاستلام.</span><span class="sxs-lookup"><span data-stu-id="86f0e-149">In both cases, the serial numbers are known before the receipt.</span></span> <span data-ttu-id="86f0e-150">بالتالي، على الجانب الداخلي، عليك التحقق من أنك قد استلمت ما يُفترض أنك قد استلمته.</span><span class="sxs-lookup"><span data-stu-id="86f0e-150">Therefore, on the inbound side, you just have to validate that you received what you were supposed to receive.</span></span>

<span data-ttu-id="86f0e-151">للتحقق من صحة الأرقام التسلسلية، يمكنك فتح صفحة **إدارة الأرقام التسلسلية** إما اثناء عمليه الاستلام أو في أي وقت قبل ترحيل الإيصال.</span><span class="sxs-lookup"><span data-stu-id="86f0e-151">To validate serial numbers, you can open the **Serial number management** page either during the receiving process or at any time before the receipt is posted.</span></span> <span data-ttu-id="86f0e-152">بالنسبة لكل صنف مسلسل يحتوي على أرقام تسلسلية مُسجلة مسبقًا، يتم تعيين كافة الأرقام التسلسلية تلقائيا إلى الحالة الأوليه لـ **غير مسجل** في هذه الصفحة.</span><span class="sxs-lookup"><span data-stu-id="86f0e-152">For each serialized item that has preregistered serial numbers, all the serial numbers are automatically set to an initial status of **Not registered** on this page.</span></span> <span data-ttu-id="86f0e-153">للتحقق من صحة الأرقام التسلسلية، يمكنك مسحها ضوئيا أو إدخالها.</span><span class="sxs-lookup"><span data-stu-id="86f0e-153">To validate serial numbers, you can scan or enter them.</span></span> <span data-ttu-id="86f0e-154">وبمجرد إدخال الرقم التسلسلي، يقوم التطبيق بالتحقق مما إذا كانت تتطابق مع الأرقام التسلسلية المُسجلة مسبقًا ام لا.</span><span class="sxs-lookup"><span data-stu-id="86f0e-154">As serial number are entered, the application validates whether they match preregistered serial numbers.</span></span> <span data-ttu-id="86f0e-155">وفي حاله مطابقتها، يتم تغيير الحالة الخاصة بها إلى **قيد التسجيل**.</span><span class="sxs-lookup"><span data-stu-id="86f0e-155">If they match, their status is changed to **Registering**.</span></span> <span data-ttu-id="86f0e-156">وإلا، ستتلقى رسالة خطأ.</span><span class="sxs-lookup"><span data-stu-id="86f0e-156">Otherwise, you receive an error message.</span></span> <span data-ttu-id="86f0e-157">الحد الأقصى لعدد الأرقام التسلسلية التي يمكنك التحقق من صحتها في القائمة يساوي كميه الاستلام.</span><span class="sxs-lookup"><span data-stu-id="86f0e-157">The maximum number of serial numbers that you can validate in the list equals to the receiving quantity.</span></span>

<span data-ttu-id="86f0e-158">يمكنك أيضا التحقق من صحة الأرقام التسلسلية على علامة تبويب **جميع الأصناف المتسلسلة** في صفحة **إدارة الأرقام التسلسلية**.</span><span class="sxs-lookup"><span data-stu-id="86f0e-158">You can also validate serial numbers on the **All serialized items** tab of the **Serial number management** page.</span></span> <span data-ttu-id="86f0e-159">في هذه القائمة، حدد الصنف الذي تريد التحقق من صحة الأرقام التسلسلية مقابله.</span><span class="sxs-lookup"><span data-stu-id="86f0e-159">In the list, select the item that you want to validate serial numbers against.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="86f0e-160">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="86f0e-160">Additional resources</span></span>

[<span data-ttu-id="86f0e-161">عملية المخزون الداخلية في POS</span><span class="sxs-lookup"><span data-stu-id="86f0e-161">Inbound inventory operation in POS</span></span>](https://docs.microsoft.com/dynamics365/commerce/pos-inbound-inventory-operation)